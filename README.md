# Credal Fern Configuration
Credal uses Fern for API documentation and SDK generation. Check out the docs at [https://docs.credal.ai](https://docs.credal.ai).

## Repo contents
This reposistory contains:

- Credal's [API Definition](./fern/definition)
- SDK [generators configured](./fern/generators.yml)
- MDX [Pages](./fern/docs/pages/)

## How to update the documentation

To update the documentation make a PR to this
repository. On pull-request we run `fern check`
to make sure that any edits to the documentation
are valid.

When the PR is merged, your changes will
automatically be deployed to the website.

### Local Development server

To run a local development server with hot-reloading you can run the following command

```sh
fern docs dev
```

### Hosted URL

To update your documentation on a hosted URL, run
```
# npm install -g fern-api
fern generate --docs
```
To preview your documentation, run
```
# npm install -g fern-api
fern generate --docs --preview
```
The repository contains GitHub workflows that will automatically run these commands for you. For example, when you make a PR a preview link will be auto-generated and when you merge to main the docs site will update.
