# Todo

## Planning

**Code**
- Architecture Diagram
- Write Code Standards
  - Git Workflow
  - Code Review Process
  - Linting
  - Clean Code Rules (function length, etc.)
  - Test Coverage (Github bot?)
  - Unit, Integration, E2E Tests
  - Domain Driven Design and Clean Directory Structure
  - Definitions of what goes where:
    - controller, service, validator, model, repository, interface, entity?
  - No new, only factories on .create
  - Pair programming encuraged
  - Code Conventions:
    - https://en.wikipedia.org/wiki/Naming_convention_(programming)#JavaScript
    - https://www.crockford.com/code.html
  - [SOLID](https://en.wikipedia.org/wiki/SOLID)

**Orga**
- Configure Project
  - What does a sprint look like?
  - Sprint length

**Design**
- Wireframe

### Decided

**Stack:**
- React
- TypeScript
- Express
- Jest
- Mongo/Mongoose
- Rabbit MQ/amqplib

## Tasks

### Orga

- create jira instance
- transfer mvp epics

### Setting up the server

- [signup netwise](https://www.netwise.co.uk/students/)
- add ssh keys
- install & config zsh, tmux

<br>

- register domain (on new namecheap account)
- configure dns for netwise

<br>

add dependencies:
- node
- mongo
- rabbit-mq

### Github orga

- create github orga (can be renamed)
- create private repo with:
  - accounting (spreadsheet for income & expenses: advanced by whom, date & purpose)
  - secrets (keepass file with credentials)

### Set up project base

- configure typescript setup
  - backend
  - react
- configure jest test setup (in TS)
  - backend
  - with react
- configure linting
  - backend
  - with react
