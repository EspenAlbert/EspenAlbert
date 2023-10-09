## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-10-09T05-36Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2459 | 1065 | 157 | 0
commit_fixes | 1194 | 512 | 61 | 2
commit_total | 6533 | 3202 | 689 | 8

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 60349 | 37703 | 7171 | 71
config_del | 22165 | 14559 | 4106 | 162
docs_add | 36249 | 18559 | 2267 | 20
docs_del | 12517 | 6020 | 1011 | 20
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 208621 | 107005 | 20255 | 15
python_del | 75878 | 33406 | 6883 | 2
shell_add | 774 | 676 | 49 | 0
shell_del | 232 | 232 | 10 | 0
terraform_add | 31173 | 25490 | 2473 | 4
terraform_del | 10748 | 9600 | 1138 | 2

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 5 | 0 | 0
dockerfile | 52 | 18 | 4 | 1
helm_chart | 51 | 21 | 4 | 0
pypi_package | 127 | 36 | 9 | 0
python_package | 46 | 25 | 2 | 0
terraform_module | 87 | 64 | 6 | 0
uml_diagram | 39 | 17 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0