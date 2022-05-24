FROM docker.io/library/debian:11
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
        python3-setuptools \
        python3-wheel \
        python3-pip \
# Below are part of system image
        dbus \
        python3 \
        python3-pip \
        python3-gi \
        python3-dbus \
        python3-pycurl \
        python3-requests \
        python3-flufl.lock \
        python3-netifaces \
        python3-serial \
        python3-serial-asyncio \
        python3-lxml \
        python3-pymodbus \
        squashfs-tools \
    && rm -rf /var/lib/apt/lists/*
