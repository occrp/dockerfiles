FROM python:2.7.10
MAINTAINER Friedrich Lindenberg <pudo@occrp.org>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get install -y -q --no-install-recommends \
        curl git python2.7 python-pip build-essential python-dev ruby-sass \
        libxml2-dev libxslt1-dev libpq-dev apt-utils ca-certificates \
  && apt-get clean

RUN curl -sL https://deb.nodesource.com/setup_5.x | bash -
RUN apt-get install -y -q nodejs && npm install -g bower uglifyjs
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
