# GETTING STARTED WITH GITHUB ACTIONS

## MICKEY GOUSSET, DEVOPS ARCHITECT - GITHUB

## github.com/mickeygousset

"I help customers get more devops-y"

Github is the largest developer platform on Earth
65M developers, 200M private and public repos...

#### What is Devops

DevOps is the union of people, process, and products to enable continuous delivery of value to your end users.

#### What are GitHub ACTIONS

- Custom workflows triggered on any GitHub event
  - Not just for CI/CD
- Workflows stored as `yml` files
- Live logs and visualized workflow execution
- Community powered workflows
- Linux, macOS, and Windows hosted runners
- Self hosted runners
- Built-in secret stored
- GitHub Enterprise Server support
- Any platform, any language, any cloud
- Marketplace of over 10,000 actions that you can integrate into your workflows

Events -Trigger-> Workflows -Use-> Actions

#### Why GitHub Actions is(are) important to you

- Open Source projects using GitHub Actions merged 34% more pull requests
- Open Source projects using GitHub Actions decreased tim to merge by 18%

#### Terminology

- The GitHub Actions documentation is stellar
- Events -> Triggers a workflow -> a workflow file that lives in a repository (yaml)
  - Each job you specify on a workflow file will spin up a Runner -> Runs Action and Logs Results
  - Each job has discrete steps that it follows
- Secrets -> Provide credentials or tokens to be able to be utilized by the repository or organization or environment

#### Github Runner

https://github.com/actions/runner

- runners that are open source that run the actions
- GitHub-hosted runner vs Self-hosted runner

#### Writing Your own Actions

- 3 types of Actions
  - JavaScript - best way
  - Docker
  - Composite

#### Demos

- GitHub Actions
  - New Workflow
    - Recommends a new workflow that you can integrate via GitHub Actions
    - The workflows themselves live in {root}/.github/workflows/{file} -> yaml file
    - In the GitHub panel on the web browser they will include intellisense for the yaml files for the actions
    - Search -> Actions on the marketplace
