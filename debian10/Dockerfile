FROM docker.io/library/debian:10
MAINTAINER "D.S. Ljungmark" <ljungmark@modio.se>

ARG URL=unknown
ARG COMMIT=unknown
ARG BRANCH=unknown
ARG HOST=unknown
ARG DATE=unknown

LABEL "se.modio.ci.url"=$URL  "se.modio.ci.branch"=$BRANCH  "se.modio.ci.commit"=$COMMIT  "se.modio.ci.host"=$HOST  "se.modio.ci.date"=$DATE


ENV container docker
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y -q \
	ca-certificates \
	squashfs-tools	\
        cmake \
        make \
        git \
        gcc \
        g++ \
	build-essential \
	libltdl-dev \
	python3-pip \
	python3-wheel \
	python3-dev \
	libxml2-dev \
	libxslt-dev \
	zlib1g-dev \
   && apt-get clean
