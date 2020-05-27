# CI/CD on Netlify using Travis

In `.travis.ci` there's a minimal configuration to run tests and deploy your site on Netlify

- Run tests
- Build site
- Deploy on Netlify

Netlify CLI needs to know who you are and the target site you want to deploy.

- Under `Personal access tokens`, select `New access token`.
- Enter a description and select `Generate token`.
- Copy the generated token to your clipboard (once you navigate from the page, the token cannot be seen again!) and add it ID to a `NETLIFY_AUTH_TOKEN` environment variable in Travis.ci.

To set the target site

- From the Netlify site dashboard, go to `Settings` > `General` > `Site details` > `Site information`, and copy the value for `API ID`.
- Assign the `API ID` to a `NETLIFY_SITE_ID` environment variable in Travis.ci UI.

## Run the project locally

```sh
yarn install
yarn run serve
```

## Run your tests

```sh
yarn run test
```
