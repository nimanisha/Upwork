# FSL DevOps Continuous Integration(CI) Challenge

## Part 1. (1.5 hr max)

Set up a new repository and CI pipeline using any free tier from the provider of your choosing (e.g. GitLab, GitHub, BitBucket, etcetera).

You can download the codebase from this repository from the `codebase` directory. The codebase contains a simple JavaScript application built using [create-react-app](https://create-react-app.dev/).

The CI build should be triggered for any pull-request and should run the following steps:

- Install dependencies `npm install`
- Linter (ESLint) `npm run lint`
- Formatter (Prettier) `npm  run prettier`
- Test (Jest) `CI=true npm run test`
- Build `npm run build`

The build should be successful. Please provide a couple of pull-requests to show pass or fail in the CI pipeline.

## Part 2. (30 max)

Write a concise description of how would you go about deploying this project to a public-cloud provider. Go in as much detail as you want, but try not to spend more than 30 minutes on it. Give a general overview of what resources will be required. Also, describe the process you'll use to build the infrastructure, deploy, handle different environments, etcetera. You can choose any public cloud and write a few sentences on why you use that provider.
