FROM debian:stretch-slim

WORKDIR /home/dev

RUN set -eux && \
	apt-get update && \
	apt-get install -y \
	stow \
	libncurses5 \
	libtinfo5 \
	&& mkdir armgcc \
	&& rm -rf /var/lib/apt/lists/*

COPY gcc-arm-none-eabi-9-2019-q4-major ./armgcc

RUN stow -t /usr/local armgcc

WORKDIR /home/dev/src
