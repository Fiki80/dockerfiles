.phony: all build

all: build

build: 
	docker build \
		-t dolphin-temp \
		-f Dockerfile.intel \
		--build-arg u_id=$$(id -u) \
		--build-arg g_id=$$(id -g) .
