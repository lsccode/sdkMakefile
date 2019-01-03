ROOT_DIR := $(shell pwd)/..
#SOURCE_DIR :=$(shell ls -F ../ | grep /)
SOURCE_DIR := \
uboot \
kernel \
sdk

COMPILE_DIR := $(addprefix $(ROOT_DIR)/,$(SOURCE_DIR))

.PHONY:$(COMPILE_DIR)
all:$(COMPILE_DIR) release

$(COMPILE_DIR):
	$(MAKE) --directory=$@ $(TARGET)
release:
	@echo "release"
clean:
	$(MAKE) TARGET=clean

test:
	@echo $(PWD)
	@echo $(COMPILE_DIR)
