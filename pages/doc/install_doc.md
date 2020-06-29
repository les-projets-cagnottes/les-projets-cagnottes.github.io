---
title: Install doc
sidebar: main_sidebar
permalink: install_doc.html
folder: doc
---

This page will show you how to download and install the component **les-projets-cagnottes.github.io** on your workstation.

First of all, create a **Personnal access token** on [your Github account](https://github.com/settings/tokens).

Put the value of this token inside a `JEKYLL_GITHUB_TOKEN` environment variable.

Then, run the following commands :

```bash
bundle install
bundle exec jekyll serve
```
