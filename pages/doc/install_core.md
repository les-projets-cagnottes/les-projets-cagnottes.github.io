---
title: Install core
sidebar: main_sidebar
permalink: install_core.html
folder: doc
---

This page will show you how to download and install the component **core** on your workstation.

Checkout the Github repository : `https://github.com/les-projets-cagnottes/core`

If you use a custom database name, user or password, modify default values in the file `src/main/resources/application.properties` :

```properties
[...]
spring.datasource.url=${SPRING_DATASOURCE_URL:jdbc:postgresql://localhost:5432/lesprojetscagnottes}
spring.datasource.username={SPRING_DATASOURCE_USERNAME:lesprojetscagnottes}
spring.datasource.password=${SPRING_DATASOURCE_PASSWORD:lesprojetscagnottes}
[...]
```

Create the following environment variables :

```bash
LPC_SLACK_CLIENT_ID=<ask-the-team>
LPC_SLACK_CLIENT_SECRET=<ask-the-team>
LPC_WEB_URL=http://localhost:4200
HTTP_PROXY=http://<host>:<port>
```

Run the following command :

```bash
mvn clean install spring-boot:run
```