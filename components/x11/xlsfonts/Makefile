#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"), version 1.0.
# You may only use this file in accordance with the terms of version
# 1.0 of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source.  A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2015 Aurelien Larcher
#

X11_CATEGORY=APP
include ../../../make-rules/shared-macros.mk
include $(WS_MAKE_RULES)/x11.mk

COMPONENT_NAME=         xlsfonts
COMPONENT_VERSION=      1.0.8
COMPONENT_SUMMARY=      xlsfonts - server font list displayer for X
COMPONENT_ARCHIVE=      $(COMPONENT_SRC).tar.xz
COMPONENT_ARCHIVE_HASH= sha256:807f909eace684b866fc63b3e962729c120822a6c96e051ff51cf350b3ffb6cd
COMPONENT_FMRI=         x11/diagnostic/xlsfonts
COMPONENT_LICENSE_FILE= COPYING

include $(WS_MAKE_RULES)/common.mk

# Auto-generated dependencies
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += x11/library/libx11
