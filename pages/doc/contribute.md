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

The backlog is prioritized in a [GitHub Project](https://github.com/orgs/les-projets-cagnottes/projects/6). If you wanna contribute, just pick an issue you're comfortable with and post a commentary inside it. A maintainer will assign the issue to you if it's relevant. 

Please, note that the platform was [developed by a single guy, who is not a developer](https://www.youtube.com/watch?v=MYZ67-Sh7kM). There are a lot of things to clean, fix security breaches, etc. You will encounter shitty pieces of code so please be indulgent and help me fix them :)

### Review

As new features are published in Pull Request, we need people to review changes and eventually propose better ways to implements those features. Don't hesitate to give your opinion and some proposals of improvement.

### Test

Today, a few cucumber tests are written in the core component but don't cover the whole functional perimeter. We need to expand cucumber test to every existing and future feature of the platform.

Furthermore, no automated tests are written in other projects so please, if you are comfortable with any test framework for Angular or NodeJS, propose a proof of concept and let's work together :)

### Design

We are trying to make a fast, efficient and beautiful user experience. If, by creating a theme, fix mobile compatibility, optimize UI or UX or any other mean, you can improve the platform, you're very welcome.

## How do we manage this project ?

Any code modification should be done on a fork. When your modifications are ok (=tested a least on your workstation), just submit a *Pull Request* on the **develop** branch. Be carefull with the description by adding every breaking change (environment variable to add, change of database structure, etc.).

When the Pull Request is merged, the issue will be closed and moved inside the Kanban.

{% include image.html file="doc/git_workflow.svg" url="/images/doc/git_workflow.svg" alt="Simplified git workflow" max-width="600" %}
