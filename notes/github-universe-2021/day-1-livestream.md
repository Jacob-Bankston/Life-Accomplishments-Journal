# GITHUB UNIVERSE - DAY 1 - LIVESTREAM

- Works on my machine - meme
- These issues don't happen because of lack of knowledge or understanding, it's because there are continuous changes 

## codespaces

Within code space you can launch a code editor within github that has all the resources within the code space in the browser. This is an IDE solution for having your containers and dev team working on the same exact thing at the same time.

Super cool stuff!

They moved all of the Github development into codespaces

### how to start working with codespaces

- Command Palette F1
- Add development container files
  - it will have templates autosourced to set up the structure for you
  - it will then ask which versions you'd like to use
  - then you can set up the features you want to install
    - you just click a checkbox and click okay
  - then it will create the dev container config for you
- rebuild
  - allows you to rebuild the dev container config without pushing changes to the repo

### Cost Controls

- automatic 30 min activity timeout
- max number of concurrent codespaces
- change machine type to fit your needs
- free editing experience - press '.' (github.dev - free)

### Personalization

- Settings Sync On - applies to any editor instances on the web and locally that have settings sync turned on
  - Updating to the theme you like
  - Also includes syncing the custom shortcuts or code snippets
- automatically installs dotfiles
- new github cli integrations within your terminal

## Github Issues

- Add in custom fields now
  - 5 types: text, number, date, single select, iteration
  - Examples from talk:
    - Areas
    - Releases
    - Cycles
    - Status
- You can look at in a board view instead of a table view
  - Looks like trello instead of the table view
- You can move and rerank items within the interface
- Tasks lists within the issue instead
- You can break down the feature into the overall scopes
  - You can convert task list items into their own separate issues
  - You can see the "Tracked in ____" value to show where the issue heirarchy is
- Video upload support
- New view - Timeline - this is coming soon!
- New hierarchy view coming soon!
- See the GitHub issues [roadmap](https://github.com/github/roadmap/issues) for more information

## GitHub Enterprise

- full on CI/CD deployment process that when new code is merged in, then it will stage, then deploy to production
- Compliance built into the process
- Access Control
  - Private means Private
    - No one else is going to see anything
    - Role based access control
    - Centralised account management and SSO
    - Configure which IP addresses are allowed to access your repositories
  - New Custom Roles - specific roles that can be assigned to teams or engineers
- Observability
  - Comprehensive set of audit logs
    - proactively detect threats
    - reactively detect threats
  - Audit Log found in Settings
    - Can stream the audits
- A Complete devops platform - [marketing page](https://github.com/enterprise)

## Github Releases

- Can set up the name for the release
- Can set up auto docs for the changes in the release
- You can set this to auto-publish to npm
  - You can see the full change log for the commits

## Github Copilot

- Leverages code that exists on the internet, and it runs an AI to pull in suggestions and create the code structure that you're wanting to set up
- AI pair programmer for developers
  - Bringing the collective wisdom of the world's developers to you
- GitHub Next - explores the frontiers of software engineering
- To get the best out of Copilot you need to be very very specific
- For those that have the tool implemented, more than 30% of the code is created by copilot