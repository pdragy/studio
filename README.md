## Installation

## Desktop

In the Release section in Github, download the latest installer for your platform (only Windows and Linux available).

To build the Desktop application, see CONTRIBUTING.md

## Docker

Instructions to run the web version of trillium locally.

Build the container image:
```
docker build -t tri .
```

Run the container:
```
docker run --rm -it -p 8080:8080 tri
```

Then visit http://localhost:8080 in your browser.

## History and related projects

Trillium is a fork of Foxglove, and Foxglove was built/copied from [webviz](https://github.com/cruise-automation/webviz). Last known release of open-sourced Foxglove studio v1 before it was deleted and taken private was 1.87.0, and last known commit was [56620d2](https://github.com/pdragy/trillium/commit/56620d28a684503a50f6c793b41b11e968b08254)

Foxglove v1 is availabile under the [Mozilla Public License v2.0](https://github.com/pdragy/trillium/blob/56620d28a684503a50f6c793b41b11e968b08254/LICENSE).

[Lichtblick](https://github.com/lichtblick-suite/lichtblick), maintained by BMW, became the parent of all foxglove/studio forks when foxglove/studio was deleted. Lichtblick was forked from foxglove v1.86.0.

## Support

Visit the Github discussions page for support for Trillium.

