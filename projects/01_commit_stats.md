# Commit Stats

[Checkout description here](https://commit-stats.ealbert.org/)

- Purpose: Track weekly key metrics across Github/Gitlab/AzureDevOps to see how I spend my time and how much I am contributing
- How: Every Monday morning I run the script that scans all my git repositories and counts the stats I care about. E.g. LoC, python packages, dockerfiles created, 3rd-party packages, etc.
- Extensions:
  - Toggl hours: Downloads the weekly time entries and summarize how many days I have worked, how many days I have worked on private projects, deep/shallow ratio, vacation days this year, and public holidays

## How it works?
- I hope to open source the CLI when it becomes more mature
- Flow:
1. Inputs: author-emails, weeks_ago=1, skip_repos=list(Path), output_repo_path, processor_locations
2. `processor_locations` are imported and added as processors
3. GitPython finds all the repositories and all the commits between mon-sun 1 week ago and calls processors with CommitData (see [processor API](#processor-api))
4. Each processor process a commit and keeps stats. It has an `init_user_dir` for storing state across weeks. Examples:
   - `CommitTypeCounter`: use commit messages for counting features/fixes/etc
   - `CommitLOC`: use file extension to count changes and prompt user to include/exclude files with more than 200 changes. Stores the include/exclude directories and files in-between runs
   - `CommitKeyMetrics`: looks for special files, e.g., Dockerfiles/main.tf/Chart.yaml. Stores the files found in-between runs.
   - `ToggleHours`: Doesn't process commits. Downloads the weekly report from toggl, adds key metrics, and dumps a weekly summary. Keeps previous vacation and public_holidays in-between runs
5. Stats are stored in a `commit_stats.csv` and tables and graphs are created based on the data. Each row is indexed by the yyyy_WEEK_NR, e.g., `2023_03`


### Processor API
```python
from __future__ import annotations
import abc
from dataclasses import dataclass
from datetime import datetime, timezone
from pathlib import Path
from typing import Any, Protocol, Type, Callable

from git import Repo, Commit, Git, GitCommandError

def file_content(git: Git, commit: str, file: str) -> str:
    try:
        return git.show(f"{commit}:{file}")
    except GitCommandError as e:
        msg = e.stderr
        if "does not exist" in msg or "exists on disk, but not in" in msg:
            return ""
        raise e


@dataclass
class FileDiff:
    deletions: list[str]
    insertions: list[str]
    is_new: bool
    insert_count: int
    del_count: int

    def has_insert_content(self, content: str) -> bool:
        return content in "\n".join(self.insertions)


@dataclass
class CommitData:
    path: Path
    repo: Repo
    commit: Commit
    file_diffs: dict[str, FileDiff]

    @property
    def commit_dt(self) -> datetime:
        return self.commit.committed_datetime.astimezone(timezone.utc)

    @property
    def commit_message(self):
        return self.commit.message

    @property
    def commit_sha(self) -> str:
        return self.commit.hexsha

    @property
    def repo_dir_name(self) -> str:
        return self.path.name

    def read_file(self, path: str) -> str:
        return file_content(self.repo.git, self.commit_sha, path)


class MetricsCall(Protocol):
    def __call__(self, rows: list[dict]) -> dict[str, float]:
        raise NotImplementedError


_processors = []
MetricGrouper = Callable[[str], str | None | tuple[str, str]]


class Processor(abc.ABC):
    def __init_subclass__(cls, **kwargs):
        if cls.__name__ != "Processor":
            _processors.append(cls)

    @classmethod
    def get_classes(cls) -> list[Type[Processor]]:
        return _processors

    @property
    def user_dir(self) -> Path:
        return self.__base_dir__

    @property
    def metric_groupers(self) -> list[MetricGrouper]:
        return []

    @property
    def user_file_yaml(self):
        return self.__base_dir__ / f"{type(self).__name__}.yaml"

    def set_base_dir(self, user_dir: Path):
        self.__base_dir__ = user_dir

    def add_commit(self, data: CommitData) -> None:
        raise NotImplementedError

    def add_stats(self, start: datetime, end: datetime) -> dict[str, float]:
        raise NotImplementedError

    def key_metrics_cols(self) -> list[str]:
        """if the value "reset" every week"""
        return []

    def accumulate_key_metrics_cols(self) -> list[str]:
        """if the value doesn't "reset" every week"""
        return []

    def key_metrics(self, rows: list[dict]) -> dict[str, float]:
        """e.g., summing up all commits"""
        return {}

    def init_user_dir(self):
        pass

    def dump_output_repo(self, path: Path, start: datetime, end: datetime) -> Any:
        pass
```
