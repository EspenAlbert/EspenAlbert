## Key metrics
<!-- KEY-METRICS:START -->
Key Metrics dumped @ `2023-08-07T07-46Z`

### Commits

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
commit_features | 2358 | 1122 | 225 | 24
commit_fixes | 1161 | 557 | 91 | 3
commit_total | 6066 | 3124 | 687 | 68

- Based on [Angular Commit message guideline](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-guidelines)

### Days/hours worked

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
break% | 4.52 | 4 | 3.77 | 4
deep_life% | 60.43 | 67.33 | 53.38 | 100
deep_work% | 78.57 | 72.79 | 65.15 | 93
life_days | 259 | 157 | 21 | 1
life_hours | 491.1 | 346.49 | 53.68 | 0.29
overtime | 368.82 | 162.92 | 23.83 | -1.03
public_holidays | 20 | 11 | 4 | 0
sick_days | 1 | 1 | 0 | 0
vacation_days | 43 | 30 | 12 | 0
work_days | 376 | 227 | 51 | 5
work_hours | 2956.9 | 1778.83 | 394.8 | 34.54

- break% is `break_time` / `total_hours`, where break_time is going to the bathroom, pomodoro break, quick snack, coffee, etc.
- deep_{life/work}% are inspired by [Cal Newport](https://www.calnewport.com/) where I track time either as _deep_ (focused work, e.g., coding, design writing, research, etc.) or _shallow_ (virtual meeting with many participants, slack chats, email replying, etc.)
- overtime is whatever `work_hours - 7.5` per day and aggregated per Δ week
- life_hours are side projects involving coding
- life_days are days where life_hours > 0

### LoC - Lines of Code deleted/added

Metric | Total | Δ 52w | Δ 13w | Δ 1w
--- | --- | --- | --- | ---
config_add | 55269 | 35242 | 10403 | 1296
config_del | 18896 | 11756 | 2589 | 489
docs_add | 34301 | 19226 | 1824 | 75
docs_del | 11722 | 5921 | 977 | 78
go_add | 274 | 0 | 0 | 0
go_del | 99 | 0 | 0 | 0
python_add | 194865 | 107151 | 29074 | 2907
python_del | 72311 | 34309 | 8843 | 2738
shell_add | 745 | 647 | 140 | 14
shell_del | 229 | 229 | 62 | 1
terraform_add | 29867 | 24977 | 5572 | 527
terraform_del | 10154 | 9114 | 1554 | 276

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
helm_chart | 47 | 19 | 1 | 0
pypi_package | 120 | 35 | 10 | 2
python_package | 46 | 27 | 3 | 1
terraform_module | 83 | 63 | 8 | 0
uml_diagram | 39 | 22 | 0 | 0
<!-- KEY-METRICS:END -->
- `pypi_package` are 3rd party packages used, see list in [requirements.txt](./requirements.txt)
- `python_package` are local packages I have created


## Commit Stats graphs
![img.png](graph.png)
- where deep_work% > 0