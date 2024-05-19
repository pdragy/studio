
## Installation

Requirements:

* node
* yarn

Run live development server, default port 8080.

```
yarn run web:serve
```

Build production server

```
yarn run web:build:prod
```

Run "storybook", default port 9009:
```
yarn storybook
```

## Docker

The build uses a multi-stage Dockerfile. First it builds the prod node app, then copies app files into caddy container which is used to serve the app. Does not do a good job of caching, so it's fastest to develop with the node/yarn tooling.

Build the container image:

```
docker build -t foxglove .
```

Run the container interactively, with the default layout on default port 8080:
```
docker run --rm -it -p 8080:8080 foxglove
```

OR Run the container, mounting a custom layout in the current directory, and serving on port 8081
```
docker run --entrypoint= --rm -it -p 8081:8081 -v $PWD/foxglove-layout.json:/foxglove/default-layout.json /bin/sh -c "caddy file-server --listen :8081"
```

> [!NOTE]
> Below here lies the old README for foxglove-studio, which is now archived. The links and information may not be relevant, and will soon be removed.

> [!NOTE]
> Foxglove Studio 1.x is no longer supported. To install the latest release, please visit our [downloads page](https://foxglove.dev/download). Learn more in our [Foxglove 2.0 announcement](https://foxglove.dev/blog/foxglove-2-0-unifying-robotics-observability).

<div align="center">
    <h1>Foxglove Studio</h1>
    <a href="https://github.com/foxglove/studio/blob/main/LICENSE"><img src="https://img.shields.io/github/license/foxglove/studio" /></a>
    <a href="https://github.com/orgs/foxglove/discussions"><img src="https://img.shields.io/github/discussions/foxglove/community.svg?logo=github" /></a>
    <a href="https://foxglove.dev/slack"><img src="https://img.shields.io/badge/chat-slack-purple.svg?logo=slack" /></a>
    <br />
    <br />
    <a href="https://foxglove.dev/download">Download</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://docs.foxglove.dev/">Docs</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://docs.foxglove.dev/changelog">Changelog</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://github.com/orgs/foxglove/discussions">Discussions</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://foxglove.dev/slack">Slack</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://x.com/foxglove">X</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://www.linkedin.com/company/foxglovedev/">LinkedIn</a>
    <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
    <a href="https://foxglove.dev/contact">Contact</a>
  <br />
  <br />

Foxglove is a visualization and observability platform for robotics development.

  <p align="center">
    <a href="https://foxglove.dev"><img alt="Foxglove screenshot" src="/resources/screenshot.png"></a>
  </p>
</div>



## Documentation

Documentation is hosted at [docs.foxglove.dev](https://docs.foxglove.dev/).

## Support

Support for Foxglove is available via the following channels:

- [GitHub Discussions](https://github.com/orgs/foxglove/discussions)
- [Foxglove Community Slack](https://foxglove.dev/slack)
- [Contact Us](https://foxglove.dev/contact)

## License

This project is availabile under the [Mozilla Public License v2.0](/LICENSE).

Foxglove is a trademark of Foxglove Technologies Inc.
