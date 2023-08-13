# Open Source code organization & workflows
- Purpose: A thoughtful approach of how to organize code to maximize quality and easiness of contributing and starting new projects
- Goals
  - Minimal amount of virtualenvs
  - re-use code
  - Consistent CI
  - re-use build/lint/test/deploy scripts
  - easy upgrade of existing code
  - minimal boilerplate for new projects
  - consistent versioning
  - Easy to bootstrap a new machine

## Directory structure from `~`
```shell
~/code/
  py/ # all python code I contribute to lives here
    .env # configure which projects are being worked on
    .yaml # configure which env-vars are active
    {RepoOwner}/ # RepoOwner, e.g., EspenAlbert, pydantic
      {RepoName} # anki-md-cli, pydantic
      {root_repo}
        pants.toml
        pyproject.toml
        .gitignore
        */**/requirements.txt
        venv/
        src/
        tests/
        readme.md
      {app_repo}
        src/
        tests/
        readme.md
  tf
  go
  js
  java
  z/ # directory is synced by rclone
    archive # code archived for future reference
      py/
      tf/
      go/
      js/
    app_data # syncing data created from scripts
    configs # aws+rclone+.zprofile+.zshrc
    docker/ # compose-files used for postgres/kafka/mongo/etc.
      compose
      dockerfile
      volumes
    docs_attachments # image files and other bigger files
    docs # private docs repo for all kinds of notes (different spec)
      # also uses git to keep changes in vcs
      github # public notes in the github profile
      personal # private notes
    docs_sync # directory that syncs to my mobile-phone+reMarkable
    helm # private and public helm charts organized per helm repo
    secrets # yaml files of env-vars organized in a hierarchy and other scripts e.g., building and pushing
    scripts # bash scripts or snippets I can use later
  z_trash/ # code that doesn't need to be synced, temporary scratches, scripts, outputs
    logs # container outputs
    repos # "1st-time-clone" repos, aka. just want to see the code
    terragrunt # outputs of terragrunt
```
- Anything related to development lives in `~/code`
- One "workspace" per coding environment, e.g., `py|go|tf`
  - Supports different editors depending on the language, e.g., pycharm for python and goland for go
  - Each workspace also "attaches"
    - `z`: credentials files, reference repos, docker files++
      - `docs`: personal markdown files, e.g., meeting notes and a log
      - for files that doesn't need to live in git. Avoids seeing changes in git changed files and can re-use credentials and other scripts
      - Can use rclone and s3 to backup this directory
- Code are always organized by repository
  - `https://github.com/pydantic/pydantic` the code will live in: `~/code/py/pydantic/pydantic`
  - `https://gitlab.com/EspenAlbert/ea_code` lives in `~/code/py/EspenAlbert/ea_code`
- Other repositories that doesn't fit into a language (e.g., work)
  - `code/{project}/{RepoOwner}/{RepoName}`

## Bootstrap new machine steps
- `brew install python3.10,awscli,kubectl,rclone...`
- get credentials from password manager and
  - configure manually `~/.aws/config, ~/.aws/credentials`
  - configure manually `~/.config/rclone/rclone.conf`
- `mkdir -p code`
- `cd code`
- `rclone sync code:z-bucket z`
- `mkdir -p py && cd py`
- todo: working on some tooling for making bootstrap of python environment easier and cloning git repos
