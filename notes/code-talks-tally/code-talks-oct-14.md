# CODE TALKS - HASHICORP USER GROUP

## Introduction to the HashiCorp tooling

### UTILITY

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

### History

- Vagrant (Written in Go, the pre-docker container/vm solution)
- Docker - Container around your application
- Packer - Define a machine image that you would want to run on AWS, GCP or Azure
  - Define your images in JSON or HCL
