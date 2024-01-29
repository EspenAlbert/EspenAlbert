## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2024-01-29T01-47Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2598 | 778 | 125 | 4
commit_fixes | 1245 | 292 | 48 | 1
commit_total | 6946 | 2481 | 372 | 10

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64333 | 29905 | 3555 | 0
config_del | 23470 | 9768 | 1045 | 0
docs_add | 36843 | 10837 | 542 | 20
docs_del | 12935 | 4365 | 377 | 204
go_add | 5217 | 4943 | 3571 | 780
go_del | 517 | 418 | 415 | 71
python_add | 223405 | 91446 | 13658 | 647
python_del | 81437 | 28807 | 5481 | 78
shell_add | 854 | 332 | 78 | 0
shell_del | 248 | 114 | 16 | 0
terraform_add | 36065 | 17827 | 4298 | 0
terraform_del | 12701 | 5722 | 1788 | 0

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
dockerfile | 55 | 17 | 3 | 0
helm_chart | 51 | 15 | 0 | 0
pypi_package | 138 | 46 | 10 | 0
python_package | 46 | 10 | 0 | 0
terraform_module | 92 | 39 | 4 | 0
uml_diagram | 39 | 7 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0