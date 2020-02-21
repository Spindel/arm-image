IMAGE_REPO = registry.gitlab.com/modioab/arm-image
IMAGE_TAG_PREFIX = debian9
IMAGE_FILES = rootfs.tar

include ../build.mk

rootfs.tar:
	./generate-arm-rootfs.sh
