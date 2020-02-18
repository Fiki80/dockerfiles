FROM debian:buster-slim

WORKDIR /home/dev

RUN set -eux && \
	apt-get update && \
	apt-get install -y \
	stow \
	&& ln -s /lib/x86_64-linux-gnu/libncursesw.so.6 /lib/x86_64-linux-gnu/libncurses.so.5 \
    && ln -s /lib/x86_64-linux-gnu/libtinfo.so.6 /lib/x86_64-linux-gnu/libtinfo.so.5 \
	&& mkdir armgcc

COPY gcc-arm-none-eabi-9-2019-q4-major ./armgcc

RUN stow -t /usr/local armgcc

WORKDIR /home/dev/src
