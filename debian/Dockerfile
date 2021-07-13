ARG IMAGE_NAME="rewardenv/docker-toolbox"
ARG IMAGE_TAG="debian-buster-slim"
FROM ${IMAGE_NAME}:${IMAGE_TAG}

RUN set -eux \
  && apt-get update && apt-get install -y --no-install-recommends \
     python3 \
     python3-pip \
  && pip3 install --no-cache-dir \
     awscli \
  && curl -fsSLo /tmp/google-cloud-sdk.tar.gz \
     https://dl.google.com/dl/cloudsdk/release/google-cloud-sdk.tar.gz \
  && mkdir -p /usr/local/gcloud \
  && tar -C /usr/local/gcloud -xvf /tmp/google-cloud-sdk.tar.gz \
  && /usr/local/gcloud/google-cloud-sdk/install.sh --quiet \
  && rm -f /tmp/google-cloud-sdk.tar.gz \
  && rm -rf /var/lib/apt/lists/*

ENV PATH $PATH:/usr/local/gcloud/google-cloud-sdk/bin