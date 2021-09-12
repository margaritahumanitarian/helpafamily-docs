---
description: >-
  Optional setup for people deploying their own instance of Help-a-Family to
  their org
---

# Lighthouse CI

Lighthouse is a tool for testing page speed and performance. We use it with a GitHub action to performance-test pull requests.

### Target Audience: Other Nonprofit Organizations

This info is only for those who are deploying a production instance of Help-a-Family. 

It's not necessary for most developers contributing to Help-a-Family to follow these instructions.

### Getting a Lighthouse CI GitHub App Token

When setting up this project for your GitHub organization, you'll need to add `LHCI_GITHUB_APP_TOKEN` to the project's Settings on GitHub.

First, generate your token by installing the Lighthouse CI app: [https://github.com/apps/lighthouse-ci](https://github.com/apps/lighthouse-ci)

![Click the &quot;Configure&quot; button](../.gitbook/assets/2021-09-12-at-12.43.36.png)

Install Lighthouse CI to only the helpafamily repo for your org:

![Only select the helpafamily repo](../.gitbook/assets/2021-09-12-at-12.46.07.png)

Copy-paste the `LHCI_GITHUB_APP_TOKEN` to your .env file so you don't lose it:

![Copy the token from here](../.gitbook/assets/2021-09-12-at-12.46.51.png)

Add the new repo secret:

![Click &quot;New repository secret&quot;](../.gitbook/assets/2021-09-12-at-12.49.32.png)

Paste your secret in:

![Paste it and click &quot;Add secret&quot;](../.gitbook/assets/2021-09-12-at-12.50.27.png)

Your secret should now show up:

![See it under &quot;Repository secrets&quot;](../.gitbook/assets/2021-09-12-at-12.52.06.png)





