# confd

* [Travis CI: ![Build Status](https://travis-ci.org/snw35/confd.svg?branch=master)](https://travis-ci.org/snw35/confd)
* [Dockerhub: snw35/confd](https://hub.docker.com/r/snw35/confd)

Automatically updated confd container.

## How To Use

This container complies with the official image specifications and runs `confd` as its default entrypoint. Template directories can be mounted as volumes or bind-mounted into the image and confd run against them:

```
docker run -it --rm -e VAR=value --mount type=bind,src=/data,dst=/data snw35/confd:latest confd -config-file "config.toml" -onetime -backend env
```
