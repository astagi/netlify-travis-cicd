# CI/CD with TravisCI and Netlify

This is a repository to experiment CI/CD with TravisCI and Netlify, configuring TravisCI to run tests, build site and then deploy on Netlify. For more about CI/CD with TravisCI and Netlify [read this article](https://dev.to/astagi/continuous-integration-and-deployment-with-travisci-and-netlify-4294).

First you need to disable automatic builds in Netlify site dashboard under `Build & Deploy` > `Continuous Deployment` > `Build settings`. Without this feature I prefer having a separate instance on Netlify to easily keep features like site preview on pull requests

- [Production site](https://frosty-lamarr-758586.netlify.app/)
- [Preview site](https://happy-galileo-9b98e8.netlify.app/)

TravisCI uses [Netlify CLI](https://docs.netlify.com/cli/get-started/) to deploy your site as you can see in `.travis.yml` configuration file. Netlify CLI needs to know who you are and the target site you want to deploy.

- Under `Personal access tokens`, select `New access token`.
- Enter a description and select `Generate token`.
- Copy the generated token to your clipboard (once you navigate from the page, the token cannot be seen again!) and add it to a `NETLIFY_AUTH_TOKEN` environment variable in TravisCI.

To set the target site

- From the Netlify site dashboard, go to `Settings` > `General` > `Site details` > `Site information`, and copy the value for `API ID`.
- Assign the `API ID` to a `NETLIFY_SITE_ID` environment variable in TravisCI UI.

## Run the project locally

```sh
yarn install
yarn serve
```

## Run your tests

```sh
yarn test:unit
```
