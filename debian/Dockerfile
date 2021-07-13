ARG IMAGE_NAME="rewardenv/docker-toolbox"
ARG IMAGE_TAG="debian-buster-slim"
FROM ${IMAGE_NAME}:${IMAGE_TAG}

RUN set -eux \
  && apt-get update && apt-get install -y --no-install-recommends \
     python3 \
     py3-pip \
  && pip3 install --no-cache-dir \
     awscli \
  && rm -rf /var/lib/apt/lists/*
