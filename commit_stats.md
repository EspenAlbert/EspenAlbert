## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-08-28T05-44Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2397 | 1061 | 192 | 12
commit_fixes | 1177 | 517 | 76 | 3
commit_total | 6276 | 3076 | 703 | 70

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 56531 | 34740 | 9081 | 300
config_del | 19771 | 12201 | 2514 | 99
docs_add | 35623 | 19205 | 2734 | 502
docs_del | 12335 | 6018 | 1489 | 229
go_add | 274 | 0 | 0 | 0
go_del | 99 | 0 | 0 | 0
python_add | 200025 | 106665 | 24700 | 1376
python_del | 74556 | 34333 | 7635 | 446
shell_add | 759 | 661 | 154 | 0
shell_del | 230 | 230 | 63 | 0
terraform_add | 30291 | 24608 | 5701 | 0
terraform_del | 10392 | 9244 | 1626 | 0

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
pypi_package | 124 | 35 | 14 | 3
python_package | 46 | 26 | 3 | 0
terraform_module | 83 | 60 | 8 | 0
uml_diagram | 39 | 21 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0