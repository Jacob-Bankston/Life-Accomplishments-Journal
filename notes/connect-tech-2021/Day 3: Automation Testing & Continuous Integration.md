# Automation Testing & Continuous Integration

## Srini Santhana

### Description

Automation testing has been near and dear to web developers. Cypress usage is on the rise exponentially.

In this lecture, we will see how to set up Cypress, write test cases, set up a dashboard to review tests, and finally integrate with the deployment tool Jenkins for continuous integration.

### Thoughts

- srini@authorify.com - always hiring - React, Node.js, MongoDB, AWS

### What's Cypress.io

- A tool for reliably testing anything that runs in web browser
- Framework agnostic
  - Angular React Vue
- Free and Open Source - MIT License
- Cypress enables you to write all types of tests:
  - End-to-end tests, integration tests, Unit tests
- Cypress runs in Browser

### Why Cypress.io

- Cypress does not use Selenium
- Cypress focuses on doing end-to-end testing REALLY well
- Cypress works on any front-end framework or website
- Cypress tests are only written in JavaScript
- Cypress is all in one
- Cypress is for developers and QA engineers - test driven development
- Cypress runs much, much faster

### Cypress.io Architecture

- Selenium runs remote commands through network
- Cypress sits on the browser itself
- Cypress has Node.js as background
- Has access to both backend and frontend
  - DOM and Network

### Live Demo

- The main goal is to simulate what the customer is doing
  - `cy.visit`
  - `cy.get`
  - `cy.get().should.last().should()`
  - `cy.contains().parent().find().check()`
- It runs through the tests on the left side of the demo, and shows the display of what the user sees on the right
- cypress has a built in wait, so you don't necessarily have to tell it to wait for things

### Continuous Integration - Cypress.io

- Integration with Jenkins
- Will save video recordings whenever you deploy to see the approved tests within the application

### Migration / Getting Started Strategy

- Always Start Small
- Build into the culture
  - Add tasks and story points the User Stories
- Use in new projects
- No big bang
