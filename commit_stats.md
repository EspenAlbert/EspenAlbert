## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-09-04T06-45Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2408 | 1062 | 178 | 11
commit_fixes | 1181 | 509 | 69 | 4
commit_total | 6304 | 3065 | 667 | 28

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 56910 | 34291 | 5544 | 379
config_del | 20291 | 12686 | 2920 | 520
docs_add | 35728 | 18678 | 2439 | 105
docs_del | 12351 | 5962 | 1314 | 16
go_add | 1646 | 1372 | 1372 | 1372
go_del | 102 | 3 | 3 | 3
python_add | 200716 | 103942 | 15981 | 691
python_del | 74639 | 33660 | 7025 | 83
shell_add | 759 | 661 | 154 | 0
shell_del | 230 | 230 | 63 | 0
terraform_add | 30572 | 24889 | 2830 | 281
terraform_del | 10552 | 9404 | 1139 | 160

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
dockerfile | 49 | 15 | 2 | 1
helm_chart | 48 | 18 | 1 | 1
pypi_package | 125 | 36 | 11 | 1
python_package | 46 | 26 | 3 | 0
terraform_module | 83 | 60 | 5 | 0
uml_diagram | 39 | 17 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0