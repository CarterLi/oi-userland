#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL)". You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2023 Andreas Wacknitz
#

BUILD_STYLE= cmake
OPENSSL_VERSION= 3.1
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		minizip-ng
COMPONENT_VERSION=	4.0.7
COMPONENT_SUMMARY=	minizip-ng is a zip manipulation library written in C
COMPONENT_PROJECT_URL=	https://github.com/zlib-ng/minizip-ng
COMPONENT_SRC=			$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=      $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_URL=  $(COMPONENT_PROJECT_URL)/archive/refs/tags/$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH=	sha256:a87f1f734f97095fe1ef0018217c149d53d0f78438bcb77af38adc21dff2dfbc
COMPONENT_FMRI=         library/$(COMPONENT_NAME)
COMPONENT_CLASSIFICATION=System/Libraries
COMPONENT_LICENSE=		BSD 3-Clause
COMPONENT_LICENSE_FILE=	LICENSE

include $(WS_MAKE_RULES)/common.mk

PATH = $(PATH.gnu)

CMAKE_OPTIONS += -DBUILD_SHARED_LIBS=yes
CMAKE_OPTIONS += -DCMAKE_INSTALL_PREFIX=/usr
CMAKE_OPTIONS += -DCMAKE_INSTALL_LIBDIR=lib/amd64
CMAKE_OPTIONS += -DCMAKE_C_FLAGS="$(CFLAGS)"
CMAKE_OPTIONS += -DMZ_BUILD_TESTS=yes
CMAKE_OPTIONS += -DMZ_BUILD_UNIT_TESTS=yes
CMAKE_OPTIONS += -DCMAKE_BUILD_TYPE=Release

unexport SHELLOPTS
COMPONENT_TEST_TRANSFORMS += '-e "s/[0-9. ]*sec//g"'

# Auto-generated dependencies
REQUIRED_PACKAGES += $(OPENSSL_PKG)
REQUIRED_PACKAGES += compress/bzip2
REQUIRED_PACKAGES += compress/xz
REQUIRED_PACKAGES += compress/zstd
REQUIRED_PACKAGES += library/zlib
REQUIRED_PACKAGES += system/library
