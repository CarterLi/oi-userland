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
# Copyright 2015 Alexander Pyhalov
# Copyright 2019 Michal Nowak
# Copyright 2022 Niklas Poslovski
#
OPENSSL_VERSION= 3.1
USE_DEFAULT_TEST_TRANSFORMS= yes
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=		nghttp2
COMPONENT_VERSION=	1.62.1
COMPONENT_SUMMARY=	HTTP/2 C Library
COMPONENT_PROJECT_URL=	https://nghttp2.org/
COMPONENT_SRC=		$(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=	$(COMPONENT_SRC).tar.xz
COMPONENT_ARCHIVE_HASH= sha256:2345d4dc136fda28ce243e0bb21f2e7e8ef6293d62c799abbf6f633a6887af72
COMPONENT_ARCHIVE_URL=	https://github.com/nghttp2/nghttp2/releases/download/v$(COMPONENT_VERSION)/$(COMPONENT_ARCHIVE)
COMPONENT_FMRI=		library/nghttp2
COMPONENT_CLASSIFICATION= System/Libraries
COMPONENT_LICENSE=	MIT
COMPONENT_LICENSE_FILE=	COPYING

include $(WS_MAKE_RULES)/common.mk

CONFIGURE_OPTIONS += --disable-static
CONFIGURE_OPTIONS += --enable-examples
CONFIGURE_OPTIONS += --disable-python-bindings
CONFIGURE_OPTIONS += --disable-app

# Manually added dependencies
TEST_REQUIRED_PACKAGES += developer/cunit
REQUIRED_PACKAGES += library/libev

# Auto-generated dependencies
REQUIRED_PACKAGES += $(GCC_RUNTIME_PKG)
REQUIRED_PACKAGES += $(GXX_RUNTIME_PKG)
REQUIRED_PACKAGES += $(OPENSSL_PKG)
REQUIRED_PACKAGES += library/jansson
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/math
