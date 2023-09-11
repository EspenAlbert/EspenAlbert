## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-09-11T07-13Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2432 | 1054 | 158 | 24
commit_fixes | 1183 | 506 | 66 | 2
commit_total | 6364 | 3065 | 651 | 60

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 57436 | 34790 | 5112 | 526
config_del | 20479 | 12873 | 2835 | 188
docs_add | 35868 | 18405 | 2347 | 140
docs_del | 12387 | 5895 | 1050 | 36
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 204376 | 104178 | 18732 | 3660
python_del | 75315 | 33768 | 7283 | 676
shell_add | 762 | 664 | 157 | 3
shell_del | 232 | 232 | 65 | 2
terraform_add | 30766 | 25083 | 2693 | 194
terraform_del | 10556 | 9408 | 1081 | 4

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
dockerfile | 49 | 15 | 2 | 0
helm_chart | 48 | 18 | 1 | 0
pypi_package | 125 | 34 | 11 | 0
python_package | 46 | 25 | 3 | 0
terraform_module | 84 | 61 | 4 | 1
uml_diagram | 39 | 17 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0