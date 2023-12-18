## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-12-18T03-05Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2521 | 878 | 89 | 0
commit_fixes | 1232 | 414 | 49 | 0
commit_total | 6804 | 2881 | 440 | 0

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 63407 | 38214 | 5971 | 0
config_del | 23439 | 14653 | 2960 | 0
docs_add | 36495 | 13343 | 627 | 0
docs_del | 12628 | 4658 | 241 | 0
go_add | 1646 | 1372 | 0 | 0
go_del | 102 | 3 | 0 | 0
python_add | 211430 | 85650 | 7054 | 0
python_del | 77488 | 26163 | 2173 | 0
shell_add | 849 | 617 | 87 | 0
shell_del | 248 | 248 | 16 | 0
terraform_add | 33879 | 23969 | 3113 | 0
terraform_del | 12223 | 9997 | 1667 | 0

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
helm_chart | 51 | 20 | 3 | 0
pypi_package | 128 | 36 | 3 | 0
python_package | 46 | 12 | 0 | 0
terraform_module | 89 | 52 | 5 | 0
uml_diagram | 39 | 8 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0