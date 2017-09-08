FROM jenkinsci/jnlp-slave
MAINTAINER Vic Iglesias <viglesias@google.com>

ENV CLOUDSDK_CORE_DISABLE_PROMPTS 1
ENV PATH /opt/google-cloud-sdk/bin:$PATH
ENV DOCKER_API_VERSION=1.23

USER root

RUN apt-get update -y
RUN apt-get install -y jq
RUN curl -fsSL https://get.docker.com/ | sh
RUN curl https://sdk.cloud.google.com | bash && mv google-cloud-sdk /opt
RUN gcloud components install kubectl
