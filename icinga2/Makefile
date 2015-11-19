DOCKER=docker
IMAGE_NAME=icinga2
INSTANCE_NAME=$(IMAGE_NAME)

build:
	$(DOCKER) build -t $(IMAGE_NAME) .

run: build
	$(DOCKER) run --rm -ti $(IMAGE_NAME)

debug: build
	$(DOCKER) run --rm -ti $(IMAGE_NAME) bash

run-daemon:
	$(DOCKER) run --name $(INSTANCE_NAME) $(IMAGE_NAME)

clean:
	$(DOCKER) rm $(INSTANCE_NAME) || true
	$(DOCKER) rmi $(IMAGE_NAME) || true
	$(DOCKER) images -q -f dangling=true | xargs $(DOCKER) rmi || true
