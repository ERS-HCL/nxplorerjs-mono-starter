# nxplorerjs-mono-starter

[![Build Status](https://travis-ci.org/ERS-HCL/nxplorerjs-mono-starter.svg?branch=master)](https://travis-ci.org/ERS-HCL/nxplorerjs-mono-starter)
[![tested with jest](https://img.shields.io/badge/tested_with-jest-99424f.svg)](https://github.com/facebook/jest)
[![DeepScan grade](https://deepscan.io/api/projects/2898/branches/21962/badge/grade.svg)](https://deepscan.io/dashboard#view=project&pid=2898&bid=21962)
[![lerna](https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg)](https://lernajs.io/)

This is a mono repo version of the [nxplorer js microservice project](https://github.com/ERS-HCL/nxplorerjs-microservice-starter)

## Workspaces

- **@nxp/nxp-core** (Core Platform)
  - The platform module which does all the configuration and setup of the server express server and GraphQL server
  - It also configures the platform components like logging, monitoring, security , IOC container
- **@nxp/nxp-server** (Application)
  - This depends on @nxp/nxp-core for all the platform requirements
  - Sets up the REST APIS, Application Services and GraphQL business API implementation

## Setup

- Execute these commands from the root directory

### Installation

```bash
yarn bootstrap
```

- Production build

```bash
yarn prepare
```

- Development mode

```bash
yarn start
```

- Unit Tests

```bash
yarn test
```

- Integration Tests

```bash
yarn itest
```

- Lint

```bash
yarn lint
```

- Serve production build
- You need to first

```bash
yarn serve
```

- Bump version
  - You can bump the version of all packages (together) using the command below
  - While it is possible to have independent versioning for individual packages. For this project we will keep all of the packages in sync as far as releases and versioning goes.

```bash
yarn release
```

## Adding new dependencies to workspaces

```bash
yarn workspace <workspace name> add <package>
```

- Example of adding node-fetch to @nxp/nxp-server

```bash
yarn workspace @nxp/nxp-server add node-fetch
```
