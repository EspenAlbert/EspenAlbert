## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-10-02T05-56Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2459 | 1065 | 169 | 18
commit_fixes | 1192 | 510 | 68 | 9
commit_total | 6525 | 3195 | 750 | 88

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 60278 | 37632 | 7544 | 1666
config_del | 22003 | 14397 | 4107 | 754
docs_add | 36229 | 18642 | 2285 | 201
docs_del | 12497 | 6000 | 1033 | 72
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 208606 | 106990 | 21297 | 2506
python_del | 75876 | 33404 | 7628 | 492
shell_add | 774 | 676 | 49 | 12
shell_del | 232 | 232 | 59 | 0
terraform_add | 31169 | 25486 | 2901 | 146
terraform_del | 10746 | 9598 | 1136 | 186

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 12 | 0 | 0
dockerfile | 51 | 51 | 3 | 2
helm_chart | 51 | 51 | 4 | 3
pypi_package | 127 | 127 | 12 | 0
python_package | 46 | 46 | 3 | 0
terraform_module | 87 | 87 | 7 | 1
uml_diagram | 39 | 39 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0