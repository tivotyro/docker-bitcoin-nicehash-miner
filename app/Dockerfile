FROM tivotyro/bitcoin-nicehash-miner:nheqminer as builder

FROM tivotyro/bitcoin-nicehash-miner:base
LABEL maintainer="tivotyro@gmail.com"

WORKDIR /app/

COPY --from=builder /app/nheqminer/Linux_cmake/nheqminer_cpu/nheqminer_cpu .
COPY --from=builder /app/nheqminer/Linux_cmake/nheqminer_cuda_tromp/nheqminer_cuda_tromp .
COPY script/ .

CMD ["/bin/bash", "start.sh"]
