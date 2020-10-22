FROM ubuntu
LABEL maintainer="tivotyro@gmail.com"

WORKDIR /app/

ENV DEBIAN_FRONTEND=noninteractive 

RUN apt-get -qq update && \
    apt-get install -qq cmake build-essential libboost-all-dev git ca-certificates iputils-ping vim --no-install-recommends < /dev/null > /dev/null
