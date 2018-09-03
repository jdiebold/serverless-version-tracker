# Serverless Version Tracker
A serverless plugin for tracking deployed versions of your code.

## Installation

#### Install using Serverless plugin manager
```bash
serverless plugin install --name serverless-version-tracker
```

#### Install using npm

Install the module using npm:
```bash
npm install serverless-version-tracker --save-dev
```

Add `serverless-version-tracker` to the plugin list of your `serverless.yml` file:

```yaml
plugins:
  - serverless-version-tracker
```

## Configuration

There is currently no configuration.

## Usage

This plugin has a super simple function: after you run `serverless deploy`, it will create a local git tag based on the version of the Lambda function that you just deployed. For instance, if your function is named `foo-production-index` and a deploy creates Lambda version 56, this plugin will automatically create a local git tag `foo-production-index-56`.

This plugin currently only runs on production deployments.

## Todo
- Enforce a clean git directory before allowing deploys (to prevent deploying untraceable / volatile code)
- Add to npm and serverless-plugin repo
- Allow configuration to run on stages other than `production`.
