# Microcks Docker Desktop Extension

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/microcks/microcks-docker-desktop-extension/build-verify.yml?branch=main&logo=github&style=for-the-badge)](https://github.com/microcks/microcks-docker-desktop-extension/actions)
[![Container](https://img.shields.io/docker/v/microcks/microcks-docker-desktop-extension?sort=semver&color=blue&logo=docker&style=for-the-badge&label=Docker.io)](https://hub.docker.com/r/microcks/microcks-docker-desktop-extension/tags)
[![License](https://img.shields.io/github/license/microcks/microcks?style=for-the-badge&logo=apache)](https://www.apache.org/licenses/LICENSE-2.0)
[![Project Chat](https://img.shields.io/badge/discord-microcks-pink.svg?color=7289da&style=for-the-badge&logo=discord)](https://microcks.io/discord-invite/)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmicrocks%2Fmicrocks-docker-desktop-extension.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmicrocks%2Fmicrocks-docker-desktop-extension?ref=badge_shield)

This extension tries to simplify the getting started experience for developers using Microcks in their local environments. This extension will start the components to run a local deployment of Microcks using container images.

For any recommendations, suggestions, feature requests and issue, head over the project's GitHub Issues tracker.

## Install

Since Docker Desktop v4.10 the extension CLI is included with the standard installation.

To install the extension:

```bash
$ docker extension install microcks/microcks-docker-desktop-extension:latest
```

## Build it locally

Build the extension image locally with `make build-extension`:

```sh
$ make build-extension
docker build --tag=microcks/microcks-docker-desktop-extension:latest .
[...]
 => => naming to docker.io/microcks/microcks-docker-desktop-extension:latest
```

Install the extension using the `docker extension` SDK and command:

```sh
$ docker extension install microcks/microcks-docker-desktop-extension:latest
```

When iterating, use the following command:

```sh
$ make build-extension && docker extension update microcks/microcks-docker-desktop-extension:latest -f
```

or see the option to just develop the frontend locally [here](https://docs.docker.com/desktop/extensions-sdk/dev/test-debug/#hot-reloading-whilst-developing-the-ui).

## Debug

Open Chrome DevTools:

```sh
docker extension dev debug microcks/microcks-docker-desktop-extension:latest
```

Developing the UI

```sh
docker extension dev ui-source microcks/microcks-docker-desktop-extension:latest http://localhost:3000
```

Reset

```sh
docker extension dev reset microcks/microcks-docker-desktop-extension:latest
```



## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmicrocks%2Fmicrocks-docker-desktop-extension.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmicrocks%2Fmicrocks-docker-desktop-extension?ref=badge_large)