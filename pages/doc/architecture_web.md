---
title: Architecture of web component
sidebar: main_sidebar
permalink: architecture_web.html
folder: doc
---

## Summary

Based on the Angular framework, the `web` component is published as a HTML / CSS / JS application. 

## Components on the root level

On the root level (the folder `src/app`), we can find main pages of the app : login, about and the app regrouping every page accessible once logged in.

There also are common tools :

- services : mainly http client used to interact with the API
- models : the object which will be manipulated through the API
- entities : it inherits from the model, it also contains associations with other entities

## Overriding environment configuration

As we need to build a package that can be deployed on multiple installations, the Angular environments mechanism does not fit our needs. Environment variables are defined in a json located at `src/assets/config.json`. A dedicated service extract those values and provide them to the project.

When deployed, this json file can be overriden as it is stored in the assets folder.

{% include links.html %}
