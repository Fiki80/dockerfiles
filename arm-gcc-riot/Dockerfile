FROM frolvlad/alpine-glibc:latest

WORKDIR /home/dev

RUN apk add --update \
	git \
	make \
	python3 \
	stow \
	&& mkdir armgcc

COPY gcc-arm-none-eabi-8-2018-q4-major ./armgcc

RUN stow -t /usr/local armgcc \
	&& git clone https://github.com/RIOT-OS/RIOT

WORKDIR /home/dev/RIOT/src
