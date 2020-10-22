FROM tivotyro/bitcoin-nicehash-miner:base
LABEL maintainer="tivotyro@gmail.com"

RUN apt-get -qq update && \
    apt-get install -qq librust-openssl-dev libcurl4-openssl-dev < /dev/null > /dev/null 

RUN git clone https://github.com/tpruvot/ccminer.git 

RUN cd ccminer/ && \
    ./autogen.sh 

RUN cd ccminer/ && \
    perl -pi.bak -e 's/_30/_61/g' Makefile.am && \
    perl -pi.bak -e 's/_30/_61/g' Makefile.in 

RUN cd ccminer/ && \
    ./configure

RUN cd ccminer/ && \
    make -j $(nproc)

#RUN cd ccminer/ && \
#    make --trace install



