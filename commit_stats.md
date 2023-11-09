## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-11-06T07-18Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2507 | 949 | 149 | 12
commit_fixes | 1219 | 443 | 58 | 9
commit_total | 6672 | 2934 | 606 | 44

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 61832 | 38061 | 6563 | 487
config_del | 22748 | 14294 | 3852 | 51
docs_add | 36365 | 15709 | 2064 | 22
docs_del | 12578 | 4807 | 856 | 0
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 210528 | 89776 | 15663 | 225
python_del | 76186 | 25928 | 3875 | 101
shell_add | 833 | 735 | 88 | 2
shell_del | 248 | 248 | 19 | 2
terraform_add | 33127 | 27237 | 3260 | 426
terraform_del | 11526 | 10134 | 1372 | 335

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
python_package | 46 | 16 | 0 | 0
terraform_module | 89 | 65 | 6 | 1
uml_diagram | 39 | 14 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0