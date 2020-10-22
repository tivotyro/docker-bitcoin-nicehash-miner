FROM tivotyro/bitcoin-nicehash-miner:base
LABEL maintainer="tivotyro@gmail.com"

RUN git clone -b Linux https://github.com/nicehash/nheqminer.git --depth=1

RUN cd nheqminer/cpu_xenoncat/Linux/asm/ \
    && sh assemble.sh \
    && cd ../../../Linux_cmake/nheqminer_cpu \
    && cmake . \
    && make -j $(nproc)

RUN cd nheqminer/Linux_cmake/nheqminer_cuda_tromp \
    && grep -v compute_20 CMakeLists.txt > CMakeLists2.txt \
    && mv CMakeLists.txt CMakeLists.txt.old \
    && mv CMakeLists2.txt CMakeLists.txt \
    && cmake . \
    && make -j $(nproc)
