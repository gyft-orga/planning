# Todo

## Planning

### Code Standards

**Process**
- Standards must be treated like rules and hence must be enforceable.
- weigh: quality vs. time spent on it
- not a one-man show, these are also Wilfredos standards

**Contents**
- Git
  - Feature Branches
  - No development branch (util we have a testing pipeline)
  - Commit adhere to [these 7 rules](https://cbea.ms/git-commit/#seven-rules)
  - A commit contains one _logical change_
  - [General background](https://who-t.blogspot.com/2009/12/on-commit-messages.html) [concrete tips](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)
  - use [Conventional Commits](https://www.conventionalcommits.org/)?
  - To come up with thoughtful commit messages, consider the following:
    - Why have I made these changes?
    - What effect have my changes made?
    - Why was the change needed?
    - What are the changes in reference to?
- Code Review
  - together?
- Linting
  - Pre-push hook
  - integrated into IDE
- Code
  - always use `const` unless `let` or `var` are specifically needed
  - no [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming))
  - no comments unless absolutely necessary (cf. clean code, comments are a
    failure to express yourself in code)
  - import/export
    - classes and functions are exported using `export`
    - classes and functions are imported using `import { Class, function } from "./directory` not the file directly
    - the `directory/index.ts` file exports all of a directories exports using `export * from "./file"`
    - TODO: add code example
  - todo:
    - rules for logging
    - rules for throwing exceptions
    - rule for Class.create factory over new Class
    - rule for controller content
    - [Clean Code Rules](https://invidious.namazso.eu/playlist?list=PLmmYSbUCWJ4x1GO839azG_BBw8rkh-zOj) (function length, etc.)
- Test Coverage
  - 90% something
  - integration for everything
  - TDD and unit tests for error prone and complicated problems (cf. [TDD vs writing tests afterwards](https://anchor.fm/fredrik-christenson/episodes/What-is-faster-on-average--TDD-or-writing-tests-after-the-code-emkkl8))
  - E2E tests (to cut down [regression testing](https://anchor.fm/fredrik-christenson/episodes/Why-do-software-developers-suck-at-regression-testing-emmgvi))
  - tests run automatically for every PR by travis
- Domain Driven Design and Clean Directory Structure
  - `test` follows the same directory structure as `src`
  - tests files have the same name as the file they are testing but `.test.ts`
  instead of `.ts` (e.g. `VatCalculator.test.ts`)
  - `src/service` includes stateless functions/classes
  - `src/repository` includes functions that access data from the database via
  ORM models
  - `src/model` ORM models
  - `src/validator` functions that validate a given input - should `throw new
  Error` or return `{error:true}` object?
  - controller, interface, entity?
- Pair programming encuraged
- Code Conventions:
  - https://en.wikipedia.org/wiki/Naming_convention_(programming)#JavaScript
  - https://www.crockford.com/code.html
- [SOLID](https://en.wikipedia.org/wiki/SOLID)

**Later if ever**
- Versioning
  - [semver](https://semver.org)

### Organization
- Configure Project
  - What does a sprint look like?
  - Sprint length
  - LICENSE: AGPL?

**Architecture**
- Architecture Diagram

### Decided

**Stack:**
- React
- Node/TypeScript, Express
- Jest
- Mongo/Mongoose
- Rabbit MQ/amqplib

## Tasks

### Setting up the server

- find alternative hosting solution (using gh student credits?)
- add ssh keys
- install & config zsh, tmux

<br>

- register domain (on new namecheap account)
- configure dns for server

<br>

add dependencies:
- node
- mongo
- rabbit-mq

### Github orga

- create private repos with:
  - accounting (spreadsheet for income & expenses: advanced by whom, date & purpose)

### Set up project base

setup in [example-project-base](https://github.com/gyft-orga/example-project-base)

- configure linting with react
- configure logger (morgan or other) [a la](https://github.com/jneidel/lock-me-out/blob/master/src/util/http-logger.ts)
