---
title: Install core
sidebar: main_sidebar
permalink: install_core.html
folder: doc
---

This page will show you how to download and install the component **core** on your workstation.

Checkout the Github repository : [https://github.com/les-projets-cagnottes/core](https://github.com/les-projets-cagnottes/core)

Create the following environment variables in your IDE launcher :

```bash
PORT=8080
SPRING_DATASOURCE_URL=jdbc:postgresql://localhost:5432/lesprojetscagnottes
SPRING_DATASOURCE_USERNAME=lesprojetscagnottes
SPRING_DATASOURCE_PASSWORD=lesprojetscagnottes
SPRING_JPA_HIBERNATE_DDL-AUTO=update
LOGGING_LEVEL_FR_LESPROJETSCAGNOTTES=DEBUG
LPC_SLACK_CLIENT_ID=<Slack Client ID>
LPC_SLACK_CLIENT_SECRET=<Slack Client Secret>
LPC_WEB_URL=http://localhost:4200
```

{% include note.html content="In these environment variables, use Slack Client ID and Slack Client Secret from [Setup Slack#Install App to the workspace](/setup_slack.html#install-app-to-the-workspace)." %}

For example, in IntelliJ, the launcher is configured the following way.

{% include image.html file="doc/core_env_vars_launcher.png" caption="Setup environment variables in an IntelliJ launcher" %}

Then, run the following command :

```bash
mvn clean install spring-boot:run
```

When the terminal print something like `Started LPCCoreApplication in 5.15 seconds (JVM running for 5.59)`, it means the core component is successfully installed and running. In the logs, you'll get default credentials for admin user. Note them in a temporary file.

The database should be initialized now. Open DBeaver and navigate to `lesprojetscagnottes > Schemas > public > Tables`. If there are a list of tables, it's OK.

{% include image.html file="doc/core_init_db.png" caption="Database structure is created" %}

Finally, you need to add stored functions in that DB. Open the file `src/main/resources/create.sql` with DBeaver and execute it.

{% include image.html file="doc/core_create_db_functions.png" caption="Create DB functions" %}

If no error pops up, it's all ready to go !
