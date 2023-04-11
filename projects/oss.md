# Open Source code organization & workflows
- Purpose: A thoughtful approach of how to organize code to maximize quality and easyness of contributing and starting new projects
- Use cases:
  - Organize open source projects in a "company-style" approach, using consistent linters/formatters/tests
  - Imagine you can start a repo and say use same linting and CI actions as the FastAPI library, e.g., `py-boot --root=https://github.com/tiangolo/fastapi https://github.com/YourUsername/AwesomeProject`
  - And later sync with their updated requirements `py-boot sync`
  - Ideally, libraries could understand better how there code is being used by clients and see if there are breaking changes
- Goals
  - Minimal amount of virtualenvs
  - re-use code
  - Consistent CI
  - re-use build/lint/test/deploy scripts
  - easy upgrade of existing code
  - minimal boilerplate for new projects
  - consistent versioning
  - Easy to bootstrap a new machine
- How?
  - Assume [pants](https://www.pantsbuild.org/docs) is installed
  - Generate pants.toml and helps syncing other files needed by pants and configuring the build sources roots
  - spits out .env files that can be loaded before running pants

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
    docs # private docs repo for all kinds of notes (different spec)
      github # public notes in the github profile
      personal # private notes
    helm # private and public helm charts organized per helm repo
    phone-sync # directory that syncs to my mobile-phone
    repos # repos used as reference
    secrets # yaml files of env-vars organized in a hierarchy and other scripts e.g., building and pushing
    scripts # bash scripts or snippets I can use later
    terragrunt # outputs of terragrunt
  z_trash/ # code that doesn't need to be synced, temporary scratches, scripts 
    logs # container outputs
    repos # "1st-time-clone" repos, aka. just want to see the code
```
- Anything related to development lives in `~/code`
- One "workspace" per coding environment, e.g., `py|go|tf`
  - Supports different editors depending on the language, e.g., pycharm for python and goland for go
  - Each workspace also "attaches"
    - `z`: credentials files, reference repos, docker files++
      - `docs`: personal markdown files, e.g., meeting notes and a log
      - for files that doesn't need to live in git. Avoids seeing changes in git changed files
- Code in: `https://github.com/pydantic/pydantic` the code will live in: `~/code/py/pydantic/pydantic`
- Code in `https://gitlab.com/EspenAlbert/ea_code` lives in `~/code/py/EspenAlbert/ea_code`
- Other repositories that doesn't fit into a language
  - `code/{project}/{RepoOwner}/{RepoName}`
  
## Bootstrap new machine steps
- `brew install python3.10,awscli,kubectl,rclone...`
- configure manually `~/.aws/config, ~/.aws/credentials`
- configure manually `~/.config/rclone/rclone.conf`
- `mkdir -p code`
- `cd code`
- `rclone sync code:z-bucket z`
- `mkdir -p py && cd py`
- `pip install virtualenv py-boot`
- `py-boot config`
- `py-boot clone`
- `py-boot sync`
- `open pycharm ~/code/py`

## Problems:
1. Split between work and private...
   - Will have to make this explicit and use .env to workon different projects at the same time
   - And avoid any dependencies in-between
   - What about the `py` repo/workspace, all those files in _tools/ is it possible to make them all shared?
   - What about the requirements.txt?
   - How do you sync these files?
   - For every "workspace"
     - Specify
       - pants.toml
       - pyproject.toml
       - resolver_name
       - venv name
   - Attempt to package tools and publish them? Or run them by local filenames always?
2. contributor that wants to bootstrap
   1. pip install py-boot
   2. py-boot configure <-- ask questions such as which IDE are you using? install pants?
      - user choices are stored in app_directory
        - ide=pycharm|vscode
        - run=repo|tree|pwd
          - local=only run pants for the current repo
          - tree=run pants in hierarchy
          - pwd=always run from pwd, if that is tree use tree
        - context <-- awesome to have this shown in the terminal (py-boot-ea|wm)
          - each context has
          - active
            - list of active projects
          - root_repo
          - name
          - branch
      - repo choices are stored in py-boot.yaml # build_files_generation for Dockerfiles/HelmCharts/etc.
        - root_repo
   3. python -m py-boot https://github.com/EspenAlbert/py-libs ea
      - `ea` is the name of the "workon"
        - this can later be used for calling workon ea (can use ea.env <-- should be checked in two source control!)
        - should clone other repos
      - understands if your python version is incompatible
      - git clone py-base py
      - takes care of setting up 3rd-party-dependencies and syncing a venv
      - understand if devpi is configured
      - understand repo_dependency files
      - understands how to configure pycharm
      - two types of repos:
        - root-repo: self or repo_url, defines the requirements.txt file, pants.toml, etc. decides the structure for all other repos...
          - should always have in .gitignore: `venv, pants.override.toml`
          - running `pants` from root repo should work "out-of-the-box"
        - app-repo: is a repo with root-repo != self
3. how would CI work?
   1. pip install py-boot
   2. py-boot sync -> uses the current directory to read & understand the repo and clone any "root-repos" + install tools, e.g., pants, configure pants.toml, configure pyproject.toml++
      - if the current repo is an app-repo it will clone the root-repo put current-repo in a different directory before configuring pants.toml++
   3. the rest of the CI script becomes:
      1. lnv
      2. pants test :: # or other commands you want to run in the CI
4. more commands
   - git commands `checkout|pull|push|clone`
   - `py-boot new {repo_url} --root=url-to-root` start a new repo