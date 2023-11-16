## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-11-13T07-50Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2511 | 936 | 136 | 4
commit_fixes | 1227 | 442 | 58 | 8
commit_total | 6706 | 2941 | 583 | 34

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 62853 | 38967 | 7298 | 1021
config_del | 23284 | 14823 | 4342 | 536
docs_add | 36427 | 15550 | 1370 | 62
docs_del | 12603 | 4831 | 513 | 25
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 210650 | 88416 | 13042 | 122
python_del | 77243 | 26676 | 3737 | 1057
shell_add | 835 | 701 | 77 | 2
shell_del | 248 | 248 | 19 | 0
terraform_add | 33683 | 27637 | 3393 | 556
terraform_del | 12173 | 10768 | 1782 | 647

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 4 | 0 | 0
dockerfile | 52 | 17 | 4 | 0
helm_chart | 51 | 21 | 4 | 0
pypi_package | 128 | 36 | 8 | 0
python_package | 46 | 15 | 0 | 0
terraform_module | 89 | 63 | 6 | 0
uml_diagram | 39 | 14 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0