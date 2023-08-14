## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-08-14T07-11Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2375 | 1086 | 197 | 17
commit_fixes | 1169 | 535 | 82 | 8
commit_total | 6123 | 3040 | 624 | 57

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 55555 | 34487 | 9230 | 286
config_del | 18942 | 11531 | 1946 | 46
docs_add | 35057 | 19392 | 2460 | 756
docs_del | 12090 | 6062 | 1303 | 368
go_add | 274 | 0 | 0 | 0
go_del | 99 | 0 | 0 | 0
python_add | 197608 | 106553 | 29185 | 2743
python_del | 73506 | 34190 | 8938 | 1195
shell_add | 758 | 660 | 153 | 13
shell_del | 229 | 229 | 62 | 0
terraform_add | 30290 | 24854 | 5747 | 423
terraform_del | 10391 | 9318 | 1644 | 237

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 6 | 0 | 0
dockerfile | 48 | 15 | 1 | 0
helm_chart | 47 | 18 | 1 | 0
pypi_package | 120 | 34 | 10 | 0
python_package | 46 | 26 | 3 | 0
terraform_module | 83 | 61 | 8 | 0
uml_diagram | 39 | 22 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0