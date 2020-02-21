IMAGE_REPO = registry.gitlab.com/modioab/arm-image/debian9
IMAGE_FILES = rootfs.tar

include ../build.mk

rootfs.tar:
	./generate-arm-rootfs.sh
