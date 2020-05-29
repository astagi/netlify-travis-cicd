# CI/CD with TravisCI and Netlify

[![Netlify Status](https://api.netlify.com/api/v1/badges/7886dc92-808d-4ce2-8189-6b36056c554e/deploy-status)](https://app.netlify.com/sites/frosty-lamarr-758586/deploys)
[![Build Status](https://travis-ci.org/astagi/netlify-travis-cicd.svg?branch=master)](https://travis-ci.org/astagi/netlify-travis-cicd)

This is a repository to experiment CI/CD with TravisCI and Netlify, configuring TravisCI to test, build and then deploy your website on Netlify. For more about CI/CD with TravisCI and Netlify [read this article](https://dev.to/astagi/continuous-integration-and-deployment-with-travisci-and-netlify-4294).

First you need to disable automatic builds in Netlify site dashboard under `Build & Deploy` > `Continuous Deployment` > `Build settings`. Without this option I suggest to run a separate instance on Netlify to easily keep features like site preview on pull requests (check [this pull request](https://github.com/astagi/netlify-travis-cicd/pull/2) to see how it works)

- [Production site](https://frosty-lamarr-758586.netlify.app/)
- [Preview site](https://happy-galileo-9b98e8.netlify.app/)

TravisCI uses [Netlify CLI](https://docs.netlify.com/cli/get-started/) to deploy your site as you can see in `.travis.yml` configuration file. Netlify CLI needs to know who you are and the target site you want to deploy.

- Under `Personal access tokens`, select `New access token`.
- Enter a description and select `Generate token`.
- Copy the generated token to your clipboard (once you navigate from the page, the token cannot be seen again!) and add it to a `NETLIFY_AUTH_TOKEN` environment variable in TravisCI.

To set the target site to deploy

- From the Netlify site dashboard, go to `Settings` > `General` > `Site details` > `Site information`, and copy the value for `API ID`.
- Assign the `API ID` to a `NETLIFY_SITE_ID` environment variable in TravisCI.

## Run the project locally

```sh
yarn install
yarn serve
```

## Run your tests

```sh
yarn test:unit
```
