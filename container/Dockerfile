ARG IMAGE_BUILD_FROM
FROM $IMAGE_BUILD_FROM


ARG URL=unknown
ARG COMMIT=unknown
ARG BRANCH=unknown
ARG HOST=unknown
ARG DATE=unknown

LABEL "se.modio.ci.url"=$URL  "se.modio.ci.branch"=$BRANCH  "se.modio.ci.commit"=$COMMIT  "se.modio.ci.host"=$HOST  "se.modio.ci.date"=$DATE


MAINTAINER "D.S. Ljungmark" <ljungmark@modio.se>
ENV container docker
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y -q \
        bash \
        docker.io \
        make \
        curl \
        git \
        ncurses-bin \
   && apt-get clean
