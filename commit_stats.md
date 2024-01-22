## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2024-01-22T02-18Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2594 | 815 | 131 | 12
commit_fixes | 1244 | 313 | 50 | 2
commit_total | 6936 | 2583 | 389 | 20

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64333 | 31145 | 3976 | 15
config_del | 23470 | 10127 | 1304 | 0
docs_add | 36823 | 11252 | 553 | 27
docs_del | 12731 | 4242 | 193 | 23
go_add | 4437 | 4163 | 2791 | 800
go_del | 446 | 347 | 344 | 129
python_add | 222758 | 93043 | 13460 | 2451
python_del | 81359 | 29148 | 5481 | 339
shell_add | 854 | 378 | 78 | 0
shell_del | 248 | 120 | 16 | 0
terraform_add | 36065 | 18814 | 4753 | 2
terraform_del | 12701 | 6427 | 1945 | 2

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 2 | 0 | 0
dockerfile | 55 | 17 | 3 | 0
helm_chart | 51 | 15 | 0 | 0
pypi_package | 138 | 46 | 11 | 0
python_package | 46 | 11 | 0 | 0
terraform_module | 92 | 41 | 5 | 0
uml_diagram | 39 | 7 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0