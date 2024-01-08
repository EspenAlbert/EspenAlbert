## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2024-01-08T01-17Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2558 | 843 | 99 | 10
commit_fixes | 1232 | 335 | 40 | 0
commit_total | 6862 | 2707 | 337 | 17

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64281 | 34442 | 4003 | 44
config_del | 23465 | 13132 | 1462 | 16
docs_add | 36761 | 11922 | 532 | 39
docs_del | 12684 | 4429 | 187 | 18
go_add | 2841 | 2567 | 1195 | 0
go_del | 253 | 154 | 151 | 0
python_add | 217257 | 90198 | 8651 | 1600
python_del | 79760 | 28254 | 3884 | 869
shell_add | 849 | 567 | 75 | 0
shell_del | 248 | 248 | 16 | 0
terraform_add | 35713 | 19796 | 4544 | 701
terraform_del | 12545 | 8168 | 1799 | 231

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
dockerfile | 53 | 17 | 2 | 0
helm_chart | 51 | 19 | 0 | 0
pypi_package | 137 | 45 | 10 | 0
python_package | 46 | 11 | 0 | 0
terraform_module | 91 | 45 | 4 | 0
uml_diagram | 39 | 7 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0