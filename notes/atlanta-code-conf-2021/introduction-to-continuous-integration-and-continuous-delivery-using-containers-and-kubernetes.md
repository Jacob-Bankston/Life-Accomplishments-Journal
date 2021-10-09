# INTRODUCTION TO CONTINUOUS INTEGRATION AND CONTINUOUS DELIVERY USING CONTAINERS AND KUBERNETES - NILLS FRANSSENS

I think that you can only do containers and kubernetes correctly if you have continuous delivery and continuous INTEGRATION

Nills Franssens - Cloud Solution Architect @nillsf
https://blog.nillsf.com

Containers are a way to package software + dependencies

Application Runtime binaries dependencies
\ | /
Container

Containers not only allow you to package your application code, but also package all the binaries and dependencies that are necessary for the application code to work.

Container images are pushed to a container registry so other systems can use them.

Build image -> Push image -> Registry -> Pull image -> Server / PC

From the registry in the cloud you can host your image to share with other developers or test/production server

Kubernetes is used to orchestrate containers

- Portable - Public, private, hybrid, multi-cloud
- Extensible - Modular, pluggable, hookable, composable
- Self-healing - Auto-placement, auto-restart, auto-replication, auto-scaling

There are integrations for GCP, AWS and Azure

The set up and work required to be able to integrate this solution has way less effort than other efforts that have been used in the past.

## Continuous Integration and Continuous Delivery

Continuous integration

- Practice of continuously testing and building software
- Output is a deployable artifact

Continuous delivery

- Practice of continuously releasing software
- Deploy the artifact frequently

Overall: The practice of continuously releasing the software

"The Science of Devops: Accelerate" by: Nicole Forsgren, PhD, Jez Humble and Gene Kim

- Book on the science of devops and the stats of comparing companies when they go through automated processes instead of overall large deployments

End-to-end container CI/CD pipeline

- Inner-loop (Run, Code, Validate, Debug)
- Source Code Control (SCC, Git)
- Build/CI, Integrate, test (Docker)
- CD, Deploy
- Run, Manage
- Monitoring

Container-based continuous integration

- build and test software (with or without container)
- Package in container image
- Store container image in registry

Recommend: Build and test your system on your PC in a docker container to build and test it prior to pushing it up to the 2nd phase

Dockerfiles - Basically simple structural set up of pulling in the code and setting up the structure to be able to run it

Github Actions - Can run continuous integrations within github

Two approaches for Kubernetes-based CD

- Push based
- Pull based (Git Ops - gaining traction)

Approach 1: Push-based continuous delivery

- traditional approach
- external system pushing updates to cluster
- ci build -> container registry -> release process (dev cluster, qa cluster, pre-prod cluster, prod cluster) -> external system (release pipeline)

deployment - define your application and also define the version of the application (kubernetes term)

Approach 2: Pull-based continuous delivery (GitOps)

- cluster component
- declarative state in git
- ci build -> container registry -> release process (dev cluster, aq cluster, pre-prod cluster, prod cluster)

Flux or ArgoCD -> tooling that sets up the git ops infrastructure

namespace - way to logically separate different sections of a deployment from each other (kubernetes term)

git ops only focuses on the deployment file, it will not perform the building and testing of the application

a git repo in flux is set up to tell flux which containers to monitor

## Comparing push and pull based systems

### Push based || Pull-based (GitOps)

- Access and credentials to Kubernetes API || Runs in cluster - leverage clusterRoles in
- No guaranteed declarative state || Declarative state
- Run once || Continuous (timer based)
- Can auto-promote after tests || Needs changes to config of each stage
- Configurable triggers || Pull request based triggers
- Monitor/log external system || Kubernetes-based monitoring/logging
- Cross-platform || Mainly kubernetes

It gets even better!

- Kubernetes API is extensible through CRD (Custom Resource Definition)
- Crossplane.io is a project doing infrastructure as code through k8s
- Deploy non-Kubernetes resources, through Kubernetes processes
- Define resources in YAML ->

The leverage of this can not only continuously automate the code source, but also the infrastructure around it as well

Free ebook on aks: https://aka.ms/handson-aks-book
Learning path for aks: https://aka.ms/spark-introduction-kubernetes

Jenkins is very frequently used
