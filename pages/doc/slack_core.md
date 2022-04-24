---
title: Activate Slack third app on core component
sidebar: main_sidebar
permalink: slack_core.html
folder: doc
---

Create the following environment variables in your IDE launcher :

```bash
FR_LESPROJETSCAGNOTTES_SLACK_ENABLED=true
FR_LESPROJETSCAGNOTTES_SLACK_CATCHER_URL=http://localhost:3000
FR_LESPROJETSCAGNOTTES_SLACK_CLIENT_ID=<Slack Client ID>
FR_LESPROJETSCAGNOTTES_SLACK_CLIENT_SECRET=<Slack Client Secret>
```

{% include note.html content="In these environment variables, use Slack Client ID and Slack Client Secret from [Setup Slack#Install App to the workspace](/setup_slack.html#install-app-to-the-workspace). The catcher URL corresponds to the [Slack Events Catcher module](/install_slack-events-catcher.html) " %}
