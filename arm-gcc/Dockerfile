FROM frolvlad/alpine-glibc:latest

WORKDIR /home/dev

RUN set -eux && \
	apk add --update \
	make \
	stow \
	&& mkdir armgcc

COPY gcc-arm-none-eabi-9-2019-q4-major ./armgcc

RUN stow -t /usr/local armgcc

WORKDIR /home/dev/src
