FROM nvidia/cuda:11.0-devel-ubuntu20.04
LABEL maintainer="tivotyro@gmail.com"

WORKDIR /app/

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -qy \
    && apt-get install -qy cmake build-essential libboost-all-dev git wget ca-certificates --no-install-recommends

