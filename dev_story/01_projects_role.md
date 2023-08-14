# Developer projects and roles
- For a background on how I got started see: [University and how I found programming](00_university.md)
- Below are the various years I have worked and the project highlights 

## Year 6: 2022-2023 DevOps Engineer
- Start [tracking my own commits](../projects/01_commit_stats.md) and publish them on my [Github profile](https://github.com/EspenAlbert)
- [Anki CLI](../projects/02_anki_cli.md) a python [textual](https://textual.textualize.io/) CLI for converting markdown files to [anki flashcards](https://apps.ankiweb.net/)
- Migration of git repositories and pipelines from Gitlab to Azure DevOps
- A SaaS product with multiple tenants on AWS running on EKS with [an istio sevice mesh](https://istio.io/latest/docs/) using mostly python, terraform, and AzureDevops pipelines
- A serverless observability system running multiple lambda functions, using open source collectors, and working with AWS CloudWatch logs, metrics, alarms, and dashboards + slack notifications
- A system for "lightweight" deployments, using terraform, cloud-init, letsencrypt, and an [envoy-proxy](https://www.envoyproxy.io/) to create a ready to use EC2 instance
- A SSO (single-sign-on) system containing two [FastAPIs](https://fastapi.tiangolo.com/) deployable as Istio External Authentication or as an AWS Lambda function

## Year 5: 2021-2022 DevOps Engineer
- Custom CI system written in python and terraform. Event-driven microservices using Kafka and MongoDB with a [Dash UI](https://dash.plotly.com/). Integrating with gitlab to show build statuses and run custom runners on AWS that supports "docker-compose" based testing with a custom pytest format and publishing test reports and alerts to slack.
- A GitOps based deployment system using a [kOps](https://kops.sigs.k8s.io/) managed kubernetes cluster and [Flux 2](https://fluxcd.io/flux/) with [SOPS](https://github.com/getsops/sops). Service mesh using Istio Operator. Monitoring with a modified [Telegraf-Operator](https://github.com/influxdata/telegraf-operator) to simplify sidecar injection and metrics. Local testing with [kind](https://kind.sigs.k8s.io/)

## Year 4: 2020-2021 Transition from Backend Developer to DevOps Engineer
- A python grpc api using MongoDB, postgresql, and rabbitmq to communicate with robots and frontends
- A rabbitmq consumer (bridge) forwarding messages to [ROS](https://docs.ros.org/) 
- A [dash UI](https://dash.plotly.com/) using opencv to modify pgm files and support reading writing to a grpc api
- Start using the open source build tool [pants](https://www.pantsbuild.org/docs) for linting, testing, dependency management, and packaging. Creating a few custom plugins for docker build, environment variables in docker-compose files and helm-chart exporting 
- A python service running selenium based tests by reading yaml files and using screenshots+OCR (optical character recognition) to test a flutter app

## Year 3: 2019-2020 Transition from Full Stack Developer to Backend Developer
- Move away from actively developing the javascript frontend to only review a new flutter based frontend
- Various side projects using [dash](https://dash.plotly.com/) for building UIs to manage personal finances and flashcards
- Continue building a backend in Python moving from flask-socketio to grpc and building smaller microservices with [FastAPI](https://fastapi.tiangolo.com/)
- Deployment workflows creating Docker Images, helm charts, and deploying to Kubernetes
- Using AWS and Gitlab for infrastructure and CI pipelines

## Year 2: 2018-2019 Transition from consultant to remote startup employee 
- Building a javascript frontend application with React and Redux
- Start writing more containerized application and looking into kubernetes for deployments
- [Sphinx](https://www.sphinx-doc.org/en/master/) generated documentation sites
- Start on writing a python packages for simplifying API development and testing (The biggest package have gone through 6 major versions with breaking changes)

## Year 1: 2017-2018 Starting my professional career as a Software Developer
- A fullstack application for controlling wheels in a vrep simulation. Python backend with [flask-socketio](https://flask-socketio.readthedocs.io/en/latest/) framework and celery using rabbitmq for background tasks. And a javascript react+redux frontend. Hosted on Heroku
- Part of maintaining a "smart-house" API powering a smart house with zigbee devices. `.net` backend and angular javascript frontend. 
- An udemy course: [Quick introduction to influxdb](https://www.udemy.com/course/master-timeseries-by-using-the-tick-stack-example-by-example/)
- An internal python GUI application for showing env-vars for different environments written using [Toga](https://toga.readthedocs.io/en/latest/)
