# Dockerfile for downloading deb package

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)][LICENSE]
[![Docker Pulls](https://img.shields.io/docker/pulls/tcnksm/download-deb.svg?style=flat-square)][dockerhub]

[LICENSE]: https://github.com/tcnksm/dockerfile-download-deb/blob/master/LICENCE
[dockerhub]: https://registry.hub.docker.com/u/tcnksm/download-deb/

When you write [bosh](http://bosh.io/) job which needs deb package, normally you download deb package and store it on blob store for reproducing. But you may develop on OSX. `tcnksm/download-deb` helps fetching deb packages anywhere you are. This is just simple helper image for your daily workflow :coffee:

## Supported tags

`tcnksm/download-deb` image support below tags. Link is its `Dockerfile`. 

- [`trusty` (trusty/Dockerfile)](trusty/Dockerfile)
- [`precise` (precise/Docekerfile)](precise/Dockerfile)

Tag is correspond to its ubuntu version.

## Usage

For example, if you want to fetch `librdkafka-dev` deb pacakge in current directory.

```bash
$ docker run -it -v `pwd`:/download tcnksm/download-deb:trusty librdkafka-dev
```

You need to mount directory where you want to save package into `/download` directory inside docker container.


