[<< Back to the index](index.md)

# Contribute

You do not need to be an expert or have tons of hours before you in order to contribute. Every small contribution is a piece of a greater thing

## What do we need ?

### Report bugs and propose new ideas

Every idea counts ! If you have a bug to report or a suggestion to make, please create a [New Issue in the *doc* repository](https://github.com/les-projets-cagnottes/doc/issues). Technical issues may be created in concerned repositories (core, web, slack-event-catcher) when placed in the roadmap.

### Develop new features or consolidate current version

Each release is decribed in a dedicated [Project](https://github.com/orgs/les-projets-cagnottes/projects). If you wanna contribute, just pick an issue you're comfortable with, assign it to yourself and move it inside the Project Kanban.

Moreover, the platform was [develop by a single guy, who is not a developer, in his room](https://www.youtube.com/watch?v=MYZ67-Sh7kM). There are a lot of things to clean, fix security breaches, etc. You will encounter shitty pieces of code so please be indulgent and help me fix them :)

### Review

As new features are published in Pull Request, we need people to review changes and eventually propose better ways to implements those feature. Don't hesitate to give your opinion and some proposals of improvement.

### Test

It's time for confessions : there are not any automated tests written, yet. It's not a best practice and in time, with your help, there will be. If your comfortable with any test framework for any component of the project, you're very welcome to propose a proof of concept.

Other tests that are welcome are manual ones on the test instance [valyou.herokuapp.com](https://valyou.herokuapp.com). Just play with it, try to break it and when you find something, create an issue as described before.

### Design

We are trying to make a fast, efficient and beautiful user interface here. If, by creating a theme, fix mobile compatibility, optimize UI or UX or any other mean, you can improve the platform, you're very welcome.

## What access rights do you need ?

These are the accounts you may need to contribute on this project. Please ask team members for them :)
- GitHub account granted on this organization
- A Slack Test Workspace / Account (you can join ours at testvalyou.slack.com)
- An account on the test instance [valyou.herokuapp.com](https://valyou.herokuapp.com)

## How do we manage this project ?

Wanna work on this project ? You're welcome :)

Any code modification should be done on a dedicated branch (or a fork if you're not part of the team yet) and when your modifications are ok (=tested a least on your workstation), just submit a *Pull Request* to another active member of the project. Be carefull with the description by adding every breaking change (environment variable to add, change of database structure, etc.).

When the Pull Request is merged, you can close the issue, move it inside the Kanban and pick another one.

Finally, when the release is fully tested on the test instance, a tag is created on each component and [Travis](https://travis-ci.org/les-projets-cagnottes) deploys them automatically in production.

## Technical documentation

This site is just a formal presentation of the platform. Every technical information (detailed architecture, data model, etc.) must be written in the Wiki of each component :
- [core](https://github.com/les-projets-cagnottes/core/wiki)
- [web](https://github.com/les-projets-cagnottes/web/wiki)
- [slack-events-catcher](https://github.com/les-projets-cagnottes/slack-events-catcher/wiki)

We're still kicking off the project so be indulgent with the lack of information please :)
