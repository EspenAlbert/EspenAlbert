## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-11-20T07-56Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2514 | 926 | 129 | 3
commit_fixes | 1230 | 441 | 56 | 3
commit_total | 6762 | 2975 | 556 | 56

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 63187 | 39086 | 6956 | 334
config_del | 23377 | 14808 | 3705 | 93
docs_add | 36453 | 14406 | 1332 | 26
docs_del | 12625 | 4810 | 519 | 22
go_add | 1646 | 1372 | 1372 | 0
go_del | 102 | 3 | 3 | 0
python_add | 210652 | 88168 | 12003 | 2
python_del | 77244 | 26624 | 3134 | 1
shell_add | 849 | 715 | 90 | 14
shell_del | 248 | 248 | 18 | 0
terraform_add | 33843 | 26836 | 3552 | 160
terraform_del | 12202 | 10487 | 1810 | 29

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
dockerfile | 52 | 17 | 4 | 0
helm_chart | 51 | 21 | 4 | 0
pypi_package | 128 | 36 | 7 | 0
python_package | 46 | 15 | 0 | 0
terraform_module | 89 | 60 | 6 | 0
uml_diagram | 39 | 8 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0