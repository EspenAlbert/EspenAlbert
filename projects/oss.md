# Open Source code organization & workflows
- Purpose: A thoughtful approach of how to organize code to maximize quality and easyness of contributing and starting new projects
- Goals
  - Minimal amount of virtualenvs
  - re-use code
  - re-use build/lint/test/deploy scripts
  - easy upgrade of existing code
  - minimal boilerplate for new projects
  - consistent versioning
  - Easy to bootstrap a new machine

## Directory structure from `~`
```shell
code/
  _docs # private docs repo for all kinds of notes (different spec)
    github # public notes in the github profile
    personal # private notes
  py/ # all python code I contribute to lives here
    .gitignore
    .env # configure which projects are being worked on
    .yaml # configure which env-vars are active
    pants.toml # https://www.pantsbuild.org/docs
    _tools/ # scripts for build/lint/test/deploy, any task that is not "business-specific"
      src
      tests
      docs
      readme.md
      pyproject.toml
      3rd_parties/
        {resolver_name}/
          requirements.txt
          BUILD # pants build file
    {RepoOwner}/ # RepoOwner, e.g., EspenAlbert, pydantic
      {RepoName} # anki-md-cli, pydantic
    z_py_3_9/ # virtualenv 
    z_py_3_10/ # virtualenv
  {project/company}
  tf
  go
  js
  java
  z/ # directory is synced by rclone
    archive # code deleted but handy for the future
    configs # aws+rclone+.zprofile+.zshrc
    docker # compose-files used for postgres/kafka/mongo/etc.
    helm # private and public helm charts organized per helm repo
    repos # "fast-clone" repos, aka. just want to see the code
    secrets # yaml files of env-vars organized in a hierarchy (explained later)
  z_output/ # code that doesn't need to be synced
```
- Anything related to development lives in `~/code`
- One "workspace" per coding environment, e.g., `py/go`
  - Supports different editors depending on the language, e.g., pycharm for python and goland for go
  - Each workspace also "attaches"
    - `_docs`: personal markdown files, e.g., meeting notes and a log
    - `z`: credentials files, reference repos, docker files++
- Code in: `https://github.com/pydantic/pydantic` the code will live in: `~/code/py/pydantic/pydantic`
- Code in `https://gitlab.com/EspenAlbert/ea_code` lives in `~/code/py/EspenAlbert/ea_code`
- Other repositories that doesn't fit into a language
  - `code/{project}/{RepoOwner}/{RepoName}`
  
## Bootstrap new machine steps
- `brew install python,awscli,kubectl,rclone...`
- configure manually `~/.aws/config, ~/.aws/credentials`
- configure manually `~/.config/rclone/rclone.conf`
- `mkdir -p code`
- `cd code`
- `rclone sync code:z-bucket z`
- `git clone py-base py`
- `cd py`
- `virtualenv -p python3.9 z_py3_9`
- `virtualenv -p python3.10 z_py3_10`
- `source z_py3_10/bin/activate`
- `pip install -r 3rd_parties/default/requirements.txt`
- `python _tools/src/bootstrap/clone.py`
- `python _tools/src/bootstrap/configs.py`
- `python _tools/src/bootstrap/pycharm.py`
- `open pycharm ~/code/py`
