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
# Copyright 2020 Aurelien Larcher
#

BUILD_BITS= 64
BUILD_STYLE= cmake
USE_DEFAULT_TEST_TRANSFORMS= yes
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= glm
COMPONENT_VERSION= 0.9.9.8
COMPONENT_REVISION= 1
COMPONENT_FMRI= library/math/glm
COMPONENT_CLASSIFICATION= System/Libraries
COMPONENT_SUMMARY= glm - OpenGL Mathematics, A C++ mathematics library for graphics programming
COMPONENT_PROJECT_URL= https://glm.g-truc.net
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_NAME)-$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH= sha256:7d508ab72cb5d43227a3711420f06ff99b0a0cb63ee2f93631b162bfe1fe9592
COMPONENT_ARCHIVE_URL= https://github.com/g-truc/glm/archive/$(COMPONENT_VERSION).tar.gz
COMPONENT_LICENSE= MIT
COMPONENT_LICENSE_FILE= copying.txt

include $(WS_MAKE_RULES)/common.mk

# Note that test-core_func_integer fails with gcc-13 but is ok with gcc-7 and gcc-10.
COMPONENT_TEST_TRANSFORMS += ' -e "/aborted/p" '

# Auto-generated dependencies
