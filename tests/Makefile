#*******************************************************************************
# Copyright (c) 2015-2016 VMware, Inc.  All rights reserved.
# SPDX-License-Identifier: GPL-2.0
#*******************************************************************************

TOPDIR    := ..
include common.mk

MAKEFLAGS += -I ../../env

SUBDIRS := test_libuart test_gui test_smbios

ifneq ($(BUILDENV),com32)
SUBDIRS += test_rts
endif

# Building rules
.PHONY: all $(SUBDIRS)

all: $(SUBDIRS)

$(SUBDIRS):
	@$(MAKE) -C $@
