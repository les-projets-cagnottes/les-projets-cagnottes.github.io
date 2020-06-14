---
title: Contribute
sidebar: main_sidebar
permalink: contribute.html
folder: doc
---

You do not need to be an expert or have tons of hours before you in order to contribute. Every small contribution is a piece of a greater thing.

## What do we need ?

### Report bugs and propose new ideas

Every idea counts ! If you found a bug or have a suggestion to make, please create a new issue in the [backlog repository](https://github.com/les-projets-cagnottes/backlog/issues). After examination, other issues might be created in concerned repositories ([core](https://github.com/les-projets-cagnottes/core/issues), [web](https://github.com/les-projets-cagnottes/web/issues), [slack-events-catcher](https://github.com/les-projets-cagnottes/slack-events-catcher/issues))

### Develop new features or consolidate current version

Each release is decribed in a dedicated [Project](https://github.com/orgs/les-projets-cagnottes/backlog/projects). If you wanna contribute, just pick an issue you're comfortable with, assign it to yourself and move it inside the Project Kanban.

Please, note that the platform was [developed by a single guy, who is not a developer, in his room](https://www.youtube.com/watch?v=MYZ67-Sh7kM). There are a lot of things to clean, fix security breaches, etc. You will encounter shitty pieces of code so please be indulgent and help me fix them :)

### Review

As new features are published in Pull Request, we need people to review changes and eventually propose better ways to implements those feature. Don't hesitate to give your opinion and some proposals of improvement.

### Test

Today, a few cucumber tests are written in the core component but don't cover the whole functional perimeter. We need to expand cucumber test to every existing and future feature of the platform.

Furthermore, no automated tests are written in other projects so please, if you are comfortable with any test framework for Angular or NodeJS, propose a proof of concept and let's work together :)

Other tests that are welcome are manual ones on the test instance [les-projets-cagnottes.herokuapp.com](https://les-projets-cagnottes.herokuapp.com). Just play with it, try to break it and when you find something, create an issue as described before.

### Design

We are trying to make a fast, efficient and beautiful user interface here. If, by creating a theme, fix mobile compatibility, optimize UI or UX or any other mean, you can improve the platform, you're very welcome.

## What access rights do you need ?

These are the accounts you may need to contribute on this project. Please ask team members for them;
- GitHub account granted on this organization
- A Slack Test Workspace / Account
- An account on the test instance [les-projets-cagnottes.herokuapp.com](https://les-projets-cagnottes.herokuapp.com)

## How do we manage this project ?

Any code modification should be done on a dedicated branch created from **develop**. When your modifications are ok (=tested a least on your workstation), just submit a *Pull Request* on the **develop** branch to another active member of the project. Be carefull with the description by adding every breaking change (environment variable to add, change of database structure, etc.).

When the Pull Request is merged, you can close the issue, move it inside the Kanban and pick another one.
