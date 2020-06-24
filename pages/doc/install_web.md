---
title: Install web
sidebar: main_sidebar
permalink: install_web.html
folder: doc
---

This page will show you how to download and install the component **web** on your workstation.

Checkout the Github repository : [https://github.com/les-projets-cagnottes/web](https://github.com/les-projets-cagnottes/web)

Open the file `src/environments/environment.ts` and modify the slackClientId with the Slack Client ID from [Setup Slack#Install App to the workspace](/setup_slack.html#install-app-to-the-workspace) :

```typescript
export const environment = {
  [...]
  slackClientId: '744027460679.730717520259',
  [...]
};
```

1. Install node modules : `npm install`
2. Run the Angular App : `ng serve`
3. Access the URL : [http://localhost:4200](http://localhost:4200)

If you see the interface loading, your installation of the web component is done.
