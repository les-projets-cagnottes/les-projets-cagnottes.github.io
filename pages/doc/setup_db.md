---
title: Setup Database
sidebar: main_sidebar
permalink: setup_db.html
folder: doc
---

To run the platform, you need to create an empty database for the component to store the data. The following way shows how to do it with DBeaver as a GUI client but you can do it in another way if you like.

## Create a connection in DBeaver

- Open DBeaver
- On the upper-left, clic on the "New connection" button

{% include image.html file="doc/dbeaver_create_db_create_connection.png" caption="Create connection on DBeaver" %}

- Select "PostgreSQL" type of connection and clic "Next"

{% include image.html file="doc/dbeaver_create_db_select_pg.png" caption="Select type of connection" %}

- On the next screen, leave everything as default (except if you set a password on the PostgreSQL installation) and hit "Test connection..."

{% include image.html file="doc/dbeaver_create_db_connection_settings.png" caption="Connection details" %}

- Then if the connection test is successfull, you can close the 2 windows

{% include image.html file="doc/dbeaver_create_db_connection_settings_test.png" caption="Successful test connection" %}

## Create a user and a database

- On the newly created connection, double-clic on it to enter the database server and open a new SQL editor via the top menu

{% include image.html file="doc/dbeaver_create_db_open_editor.png" caption="Open SQL Editor" %}

- In this editor, enter the following script and execute it via the button on the left

```sql
create database lesprojetscagnottes;
create user lesprojetscagnottes with encrypted password 'lesprojetscagnottes';
grant all privileges on database lesprojetscagnottes to lesprojetscagnottes;
```

{% include image.html file="doc/dbeaver_create_db_execute_script.png" caption="Execute the script" %}

- And then you're done ! You have a dedicated database for the platform accessible via lesprojetscagnottes / lesprojetscagnottes credentials
