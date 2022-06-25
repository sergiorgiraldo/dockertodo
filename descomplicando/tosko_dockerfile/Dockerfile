FROM debian

LABEL app="Girapops"
ENV SRG="THE_DEV"

RUN apt-get update && apt-get install -y stress && apt-get clean

CMD stress --cpu 1 --vm 1 --vm-bytes 64M
