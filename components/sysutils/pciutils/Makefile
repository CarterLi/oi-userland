#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2013 - 2016 Adam Stevko. All rights reserved.
#

BUILD_STYLE= justmake
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		pciutils
COMPONENT_VERSION=	3.12.0
COMPONENT_SUMMARY=	The PCI Utilities are a collection of programs for inspecting and manipulating configuration of PCI devices
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:827a641d2016a15f0b959804daa5a05f055d0f91d58a70d32ac41ce7ef94164e
COMPONENT_ARCHIVE_URL=	https://mj.ucw.cz/download/linux/pci/$(COMPONENT_ARCHIVE)
COMPONENT_PROJECT_URL=	https://mj.ucw.cz/sw/pciutils/
COMPONENT_FMRI=		system/pciutils
COMPONENT_CLASSIFICATION=	System/Hardware
COMPONENT_LICENSE=	GPLv2
COMPONENT_LICENSE_FILE=	COPYING

TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

PATH= $(PATH.gnu)

COMPONENT_BUILD_ARGS += CC=$(CC)
COMPONENT_BUILD_ARGS += OPT="-DBYTE_ORDER=1234 -DLITTLE_ENDIAN=1234"
COMPONENT_BUILD_ARGS += PREFIX="/usr"

COMPONENT_INSTALL_ARGS += PREFIX="/usr"

# Auto-generated dependencies
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += shell/ksh93
REQUIRED_PACKAGES += system/library
