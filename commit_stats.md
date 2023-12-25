## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-12-25T01-42Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2534 | 868 | 97 | 13
commit_fixes | 1232 | 403 | 49 | 0
commit_total | 6824 | 2857 | 415 | 20

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64207 | 37552 | 6518 | 800
config_del | 23439 | 14591 | 2728 | 0
docs_add | 36703 | 13062 | 814 | 208
docs_del | 12649 | 4606 | 241 | 21
go_add | 2841 | 2567 | 1195 | 1195
go_del | 253 | 154 | 151 | 151
python_add | 213744 | 87225 | 8530 | 2314
python_del | 78396 | 26950 | 3029 | 908
shell_add | 849 | 617 | 87 | 0
shell_del | 248 | 248 | 16 | 0
terraform_add | 34822 | 23875 | 4009 | 943
terraform_del | 12297 | 9967 | 1741 | 74

- python is for files ending in: ".py",".pyi"
- go is for files ending in: ".go"
- shell is for files ending in: ".sh"
- terraform is for files ending in: ".tf"
- config is for files ending in: ".yml",".yaml",".json",".hcl",".tfvars"
- docs is for files ending in: ".md",".rst"

### Other Metrics

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
design_spec | 12 | 3 | 0 | 0
dockerfile | 52 | 17 | 3 | 0
helm_chart | 51 | 19 | 3 | 0
pypi_package | 131 | 39 | 6 | 3
python_package | 46 | 12 | 0 | 0
terraform_module | 91 | 52 | 6 | 2
uml_diagram | 39 | 8 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0