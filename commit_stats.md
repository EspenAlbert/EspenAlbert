## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-09-25T05-54Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2441 | 1047 | 151 | 4
commit_fixes | 1183 | 501 | 59 | 0
commit_total | 6437 | 3107 | 663 | 28

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 58612 | 35966 | 5878 | 923
config_del | 21249 | 13643 | 3353 | 538
docs_add | 36028 | 18441 | 2110 | 139
docs_del | 12425 | 5928 | 987 | 17
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 206100 | 104484 | 18791 | 886
python_del | 75384 | 32912 | 7136 | 17
shell_add | 762 | 664 | 37 | 0
shell_del | 232 | 232 | 59 | 0
terraform_add | 31023 | 25340 | 2755 | 210
terraform_del | 10560 | 9412 | 950 | 4

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
dockerfile | 49 | 15 | 1 | 0
helm_chart | 48 | 18 | 1 | 0
pypi_package | 127 | 36 | 12 | 2
python_package | 46 | 25 | 3 | 0
terraform_module | 86 | 63 | 6 | 1
uml_diagram | 39 | 17 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0