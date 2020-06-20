---
title: Setup Slack
sidebar: main_sidebar
permalink: setup_slack.html
folder: doc
---

This is not mandatory, but Slack integration is an important feature of the platform. If you develop around it, we suggest you to create a test workspace of your own and connect your setup of the platform to it.

## Create a Slack Workspace

- First of all, visit the official [Slack website](https://slack.com/create) and follow the instructions.

- You can name it the way you want and customize it if you like, this is your personal workspace to test the integration between Slack and the platform.

## Create a Slack App

- Once the workspace created and email validated, you can visit the [Slack API](https://api.slack.com/apps) (and favorite this link).

- Next, clic on **Create New App**

{% include image.html file="doc/slack_create_app.png" caption="Create New App" %}

- Fill the required fields with an appropriate name and select the workspace you created before

{% include image.html file="doc/slack_create_app_modal.png" caption="Fill required fields" %}

## Configure the App with current settings

### Redirect URLs

In **OAuth & Permissions**, scroll down to the **Redirect URLs** and add the following :
- http://localhost:4200/login/slack
- http://localhost:4200/organizations/edit/slack/

{% include image.html file="doc/slack_oauth_permissions_redirect_urls.png" caption="Add Redirect URLs" %}

{% include important.html content="Don't forget to hit the **Save URLs** button." %}

### Scopes

In **OAuth & Permissions**, scroll down to the **Scopes** and add the following :
- Bot Token Scopes :
  * chat:write
  * app_mentions:read
  * team:read
  * users:read
  * im:write
- User Token Scopes
  * channels:write

{% include image.html file="doc/slack_oauth_permissions_scopes.png" caption="Add Scopes" %}

## Install App to the workspace

The definition of scopes allows us now to install the App in the workspace previously created. To do so, navigate to **Install App** and clic on **Install App to Workspace**

{% include image.html file="doc/slack_install_app.png" caption="Navigate to Install App" %}

Next, Slack will ask you to authorize the app with the permissions you defined in the previous part. Clic **Allow**

{% include image.html file="doc/slack_install_app_oauth.png" caption="Authorize the App" %}

Once redirected to Slack API, return to **Basic Information** and store in a temporary file values in *Client ID*, *Client Secret* and *Signing Secret*. You will use them in the installation of components.

{% include image.html file="doc/slack_install_app_tokens.png" caption="Credentials to save" %}

## Configure events

{% include important.html content="This section cannot be done before installing [slack-events-catcher](/install_slack-events-catcher.html). Please return here after." %}

In **Event Subscriptions** set the following parameters.

- Request URL : <ngrok-url>
- Subscribe to bot events
  * app_mention
  * message.im
  * user_change
- Subscribe to workspace events
  * team_join
  
{% include image.html file="doc/slack_event_subscription.png" caption="Add Redirect URLs" %}

{% include important.html content="Don't forget to hit the **Save Changes** button at the bottom of the page" %}
