## Key metrics
- Only started dumping data from 2022
- Once a week I scan all repos (public and private) from different version control sources (Github, Gitlab, etc.) and gather specific data, see [projects/01_commit_stats](projects/01_commit_stats.md) for details 
- Column explanations: 
  - Δ 52w means the last year (52 weeks)
  - Δ 13w means last quarter (13 weeks)
  - Δ 1w means the last week

<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2024-01-15T01-13Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2582 | 837 | 123 | 24
commit_fixes | 1242 | 324 | 48 | 10
commit_total | 6916 | 2639 | 383 | 54

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 64318 | 32307 | 3969 | 37
config_del | 23470 | 10349 | 1305 | 5
docs_add | 36796 | 11510 | 547 | 35
docs_del | 12708 | 4226 | 191 | 24
go_add | 3637 | 3363 | 1991 | 796
go_del | 317 | 218 | 215 | 64
python_add | 220307 | 92082 | 11686 | 3050
python_del | 81020 | 29273 | 5142 | 1260
shell_add | 854 | 378 | 80 | 5
shell_del | 248 | 120 | 16 | 0
terraform_add | 36063 | 18990 | 4890 | 350
terraform_del | 12699 | 6450 | 1951 | 154

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
dockerfile | 55 | 18 | 3 | 2
helm_chart | 51 | 16 | 0 | 0
pypi_package | 138 | 46 | 11 | 1
python_package | 46 | 11 | 0 | 0
terraform_module | 92 | 42 | 5 | 1
uml_diagram | 39 | 7 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0