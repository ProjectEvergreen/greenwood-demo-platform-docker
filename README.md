# greenwood-demo-platform-docker

This is a demonstration repo for [running Greenwood inside a NodeJS Docker container](https://www.greenwoodjs.dev/guides/hosting/#docker).

## Overview

This repo aims to demonstrate a couple of Greenwood's features ([API Routes](https://www.greenwoodjs.dev/docs/pages/api-routes/) and [SSR pages](https://www.greenwoodjs.dev/docs/pages/server-rendering/)), focused on using Web Components (WCC) and Web Standards to deliver the content for the demo.

## Usage

You can follow these steps to build the demo code in this repo to run in a Docker container.

### Building and running your application

Start your application by running:

```sh
docker compose up --build
```

The application will be available at `http://localhost:8080`.

### Deploying your application to the cloud

To build build an image, run

```sh
docker build -t myapp .
```

If your cloud uses a different CPU architecture than your development machine (e.g., you are on a Mac M1 and your cloud provider is amd64), you'll want to build the image for that platform, e.g.:

```sh
docker build --platform=linux/amd64 -t myapp .`.
```

Then, push it to your registry, e.g.

```sh
docker push myregistry.com/myapp
```

> _Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/) docs for more detail on building and pushing._

### References

- [Docker's Node.js guide](https://docs.docker.com/language/nodejs/)
- [Reference Repo](https://github.com/docker/docker-nodejs-sample)
- [Docker for Desktop](https://docs.docker.com/desktop/)