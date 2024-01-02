## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2024-01-02T03-16Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2548 | 847 | 107 | 14
commit_fixes | 1232 | 345 | 49 | 0
commit_total | 6845 | 2747 | 408 | 21

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64237 | 36348 | 5625 | 30
config_del | 23449 | 14018 | 2200 | 10
docs_add | 36722 | 12943 | 694 | 19
docs_del | 12666 | 4622 | 241 | 17
go_add | 2841 | 2567 | 1195 | 0
go_del | 253 | 154 | 151 | 0
python_add | 215657 | 88625 | 9557 | 1913
python_del | 78891 | 27395 | 3507 | 495
shell_add | 849 | 617 | 87 | 0
shell_del | 248 | 248 | 16 | 0
terraform_add | 35012 | 21817 | 3989 | 190
terraform_del | 12314 | 9735 | 1754 | 17

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
dockerfile | 53 | 17 | 4 | 1
helm_chart | 51 | 19 | 3 | 0
pypi_package | 137 | 45 | 10 | 6
python_package | 46 | 11 | 0 | 0
terraform_module | 91 | 46 | 5 | 0
uml_diagram | 39 | 8 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0