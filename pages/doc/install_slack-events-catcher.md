---
title: Install slack-events-catcher
sidebar: main_sidebar
permalink: install_slack-events-catcher.html
folder: doc
---

This page will show you how to download and install the component **slack-events-catcher** on your workstation.

{% include important.html content="This section cannot be done before installing [core](/install_core.html) and [web](/install_web.html) components. Please return here after." %}

Checkout the Github repository : [https://github.com/les-projets-cagnottes/slack-events-catcher](https://github.com/les-projets-cagnottes/slack-events-catcher)

Create a file `.env` at the root of the project and enter :

```env
PORT=3000
LPC_CORE_API_TOKEN=<API Token>
LPC_CORE_API_URL=http://localhost:8080
LPC_SLACK_SIGNING_SECRET=<Slack Signing Secret>
```

{% include note.html content="In these environment variables, use Slack Client ID and Slack Signing Secret from [Setup Slack#Install App to the workspace](/setup_slack.html#install-app-to-the-workspace)." %}

Install node modules : `npm install`

Run the App : `node src/index.js`

In another terminal, expose the App to Slack : `ngrok http 3000`

When ngrok is started, note in a temporary file the forwarding URL like in the picture

{% include image.html file="doc/ngrok_started.png" caption="Ngrok started" %}

You can now complete the installation with the [Setup Slack#Configure events](/setup_slack.html#configure-events) section.
