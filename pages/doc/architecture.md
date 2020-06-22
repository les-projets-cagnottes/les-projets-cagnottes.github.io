---
title: Architecture
sidebar: main_sidebar
permalink: architecture.html
folder: doc
---

## Summary

The platform is composed of several components communicating between each others through different channels as sumerized by the following schema.

{% include image.html file="doc/architecture_schema.svg" url="/images/doc/architecture_schema.svg" alt="Main architecture of the platform" max-width="600" %}

## Explainations

### The core

The `core` component **process all the functional part of the platform**
- user registration
- creation of a project
- contribution
- etc. 

It directly **stores its data in a PostgreSQL Database** and **exposes an API** whose structure is described with [this Swagger page](/swagger.html). In order to synchronize users with the database, it also **connect to Slack on its [Web API](https://api.slack.com/web)** when needed. The framework used for this component is *Spring Boot*.

### Events from Slack

The `slack-events-catcher` component is a small *NodeJS* project that **listen to the Slack [Events API](https://api.slack.com/events-api)** for several events :
- A user joins a Slack Team
- A user is disabled
- etc.

When conditions are met, this component call the appropriate endpoint on the `core` API.

### The user interface

The`web` component is the user interface of the platform. It is basically a **web client** grabbing data and executing functions through the `core` API. The majority of the resources are **stored in cache of web browsers** to optimize efficiency. Today, this forces us to inform user that they need to empty their cache after an update.

### This documentation

The `les-projets-cagnottes.github.io` component is managing the documentation you are reading. It also stores [Cucumber report](/cucumber.html) for the `core` component and may storing other similar static files in the future. This project is build with [Jekyll](https://jekyllrb.com/), the [tomjoht/documentation-theme-jekyll](https://github.com/tomjoht/documentation-theme-jekyll) template and hosted on [GitHub Pages](https://pages.github.com/)

### Why ?

This structure allows us to **take advantage of each involved technology** and eventually replace them independently when the time will come. It also gives us the opportunity to expand with other clients in front on the platform.

{% include links.html %}
