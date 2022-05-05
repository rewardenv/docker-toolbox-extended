# docker-toolbox-extended

A docker toolbox image based on rewardenv/docker-toolbox with these additional tools included:
- awscli
- google-cloud-sdk
- python3
- pip3
- terraform-docs

## Usage

```
docker run --rm -it rewardenv/docker-toolbox-extended bash
```

## Available tags

- latest, alpine-latest
- debian-bullseye-slim

## Build

```
DOCKER_BASE_IMAGE=debian:bullseye-slim bash -x scripts/build.sh

DOCKER_BASE_IMAGE=alpine:latest bash -x scripts/build.sh  
```
