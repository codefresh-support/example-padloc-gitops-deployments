# Gitops deployments repo
#### Project diagram
![project diagram](./diagram.png)
#### Description
Where the application monorepo represents the source of truth for the application code,  
This repository is in charge of providing the ops side of things, both CI and CD.

CI part is implemented in the form of Codefresh pipeline (Classic) and provides  
Application testing, building and pushing of artifacts, and deploying to a Dev environment for making a final decision  
on deploying the Application to the Prod environment.  

CD part is done with the help of Codefresh GitOps runtimes, one per Dev/Prod cluster.
Codefresh Environments and Products dashboards also play  an important role in providing observability on the application statuses across the environments.

This repository contains the application helm chart together with the corresponding ArgoCD application specifications for both target environments.  

