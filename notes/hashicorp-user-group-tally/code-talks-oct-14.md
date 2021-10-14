# CODE TALKS - HASHICORP USER GROUP

## Introduction to the HashiCorp tooling

### UTILITY

- **The Point:** The main advantage in the HashiCorp model is the fact that the structure is set up in the code
- **The Second Point:** Can go into the cloud devops tooling for AWS, GCP, Azure
- Open source platform, lots of market adoption
  - There are some of the products that are commercial products at this point
- Vault service used to store secrets
- Terraform - large amount of the focus of the intro talk
- Orchestration solutions via Nomad
- Nomad - continuous delivery in containers or virtual machines
  - Different to k8s because k8s is containers only, so the layer to orchestration is not as large
  - In my opinion containers is probably the way forward, but that being said, migrating to this tool would probably be easier for a company that is not as maintained and cutting edge.

### Purpose

- To be the layer between the Azure, GCP and AWS tooling to deploy to their infrastructure

### Shift in Product Management

- Self-managed: The Open Source products
- HashiCorp-managed: The paid version that becomes a SaaS offering

## Group Discussion

### Self-intros

- Several people that use HashiCorp tooling at the meetup
- Some people using GCP functions
- Some people using AWS

### History & Terminology

- Vagrant (Written in Go, the pre-docker container/vm solution)
- Docker - Container around your application
- Packer - Define a machine image that you would want to run on AWS, GCP or Azure
  - Define your images in JSON or HCL
- Orchestrator - How much compute is available leftover? Handle that situation.
  - "Here's all the requirements for the application, find me where in the resources that we can run this."
  - Spins up and spins down resources as needed for the app/server/etc...

### Structure

Layers: Terraform -> Console -> Vault -> Nomad

### Demo

- You have to have an AWS, GCP or Azure account already created
- Follow along with the README.md file
  - set up a packer.json file
    - Defines the image definition
  - use `package build`
    - runs terraform to then spin up the servers on the cloud platform

### Tech Preview Nomad Pack

- Nomad Job file
  - Large json file that sets up the config for the container that is deployed via Nomad
- They have created new templates to be reconfigured
  - One of their packs is Nginx
  - sections have been template-ized that you inject the variables into the output
- You can jump into your url in the terminal and get a UI to see the current values of your Nomad container deployment
  - Can see all of your information for all the clients
- You can reuse the templates over and over instead of maintaining several different json templates
