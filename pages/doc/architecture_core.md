---
title: Architecture of core component
sidebar: main_sidebar
permalink: architecture_core.html
folder: doc
---

## Summary

Based on the Spring Boot framework, the `core` component is built using Maven and OpenJDK. It relies on a PostgreSQL database and stores files on its filesystem.

## Sub-components in detail 

Each functional object (budget, campaign, idea, ...) has its package in `src/main/java` folder. In each one of them we create the following structure :

- a model : the object which will be manipulated through the API
- an entity : it inherits from the model, it is the object stored in DB
- a repository : the interface to interact with the DB. Defined methods respects the [JPA query lookup strategies](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods)
- a controller : entrypoints of each API endpoint
- a service : the main logic of each operation. Can be called from the controller or other components

## Data Model

{% include image.html file="doc/data_model.png" url="/images/doc/data_model.png" alt="Data Model" max-width="600" %}

This component also provides stored procedures in DB written in `src/main/resources/create.sql`.

## Tests

Automated tests are written ìn `src/test`using Cucumber.

Features are destribed in the `features` folder. Each scenario of a feature is composed of functional steps which needs to be translated in Java to perform the corresponding step. These translations are written in a `steps` package inside the `src/test/java` folder.

Finally, when API calls are required, they are implemented in HTTP clients inside a `component` package.

{% include links.html %}
