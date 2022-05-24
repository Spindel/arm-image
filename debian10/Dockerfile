FROM docker.io/library/debian:10
LABEL maintainer="ljungmark@modio.se"
ENV container docker

ARG URL=unknown
ARG COMMIT=unknown
ARG BRANCH=unknown
ARG HOST=unknown
ARG DATE=unknown

LABEL se.modio.ci.url="$URL"
LABEL se.modio.ci.host="$HOST"
LABEL se.modio.ci.date="$DATE"
LABEL se.modio.ci.branch="$BRANCH"
LABEL se.modio.ci.commit="$COMMIT"

RUN apt-get update && \
    apt-get --assume-yes --no-install-recommends install \
# Packages needed to run as a gitlab CI stage
        openssh-client \
        git \
        python3-pip \
# Build related tools, what mytemp-backend needs to compile wheels etc.
        ca-certificates \
        squashfs-tools \
        libdbus-1-3 \
        cmake \
        make \
        git \
        gcc \
        g++ \
        build-essential \
        libltdl-dev \
        python3-dev \
        libxml2-dev \
        libxslt-dev \
        zlib1g-dev \
    && rm -rf /var/lib/apt/lists/* \
# The most common thing in all consumers is to update some these python packages
    &&  /usr/bin/python3 -m pip install --upgrade pip \
    &&  /usr/bin/python3 -m pip install --upgrade wheel setuptools
