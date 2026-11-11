# Userspace UAPI snapshot; does not build or replace the stock kernel.
VERSION = 6
PATCHLEVEL = 1
SUBLEVEL = 170
HEADER_SOURCE := $(abspath $(dir $(lastword $(MAKEFILE_LIST))))
SOURCE_ROOT := $(abspath $(HEADER_SOURCE)/../../../..)
HEADER_OUTPUT := $(if $(filter /%,$(O)),$(O),$(SOURCE_ROOT)/$(O))
.PHONY: headers_install
headers_install:
	@test "$(ARCH)" = arm64
	@test -n "$(O)"
	mkdir -p $(HEADER_OUTPUT)/usr/include
	cp -a $(HEADER_SOURCE)/include/. $(HEADER_OUTPUT)/usr/include/
