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
# Copyright 2019 Alexander Pyhalov
# Copyright 2022 Marco van Wieringen
# Copyright 2024 Andreas Wacknitz
#

PG_VERSION= 16
include ../../../make-rules/shared-macros.mk

COMPONENT_NAME= citus
COMPONENT_VERSION= 12.1.4
COMPONENT_SUMMARY= Citus Open Source PostgreSQL extension
COMPONENT_SRC= $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE= $(COMPONENT_NAME)-$(COMPONENT_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH= sha256:6f8e55bbcae75309192c48cdb7238e8c895fd63e5b785ff798023c8b8b799e61
COMPONENT_ARCHIVE_URL= https://github.com/citusdata/citus/archive/v$(COMPONENT_VERSION).tar.gz
COMPONENT_PROJECT_URL= https://www.citusdata.com/
COMPONENT_FMRI= database/postgres-$(PG_VERNUM)/citus
COMPONENT_CLASSIFICATION= System/Databases
COMPONENT_LICENSE= AGPLv3.0
COMPONENT_LICENSE_FILE= LICENSE

# Don't depend on host default pg_config
PATH= $(PG_BINDIR):$(PATH.illumos)

TEST_TARGET= $(NO_TESTS)
include $(WS_MAKE_RULES)/common.mk

CONFIGURE_OPTIONS += LDFLAGS=-L$(OPENSSL_LIBDIR)
CONFIGURE_OPTIONS += CPPFLAGS=-I$(OPENSSL_INCDIR)
CONFIGURE_OPTIONS += PKG_CONFIG_PATH=$(OPENSSL_PKG_CONFIG_PATH)

# Manually added dependencies
REQUIRED_PACKAGES += $(PG_DEVELOPER_PKG)

# Auto-generated dependencies
REQUIRED_PACKAGES += $(OPENSSL_PKG)
REQUIRED_PACKAGES += $(PG_LIBRARY_PKG)
REQUIRED_PACKAGES += compress/zstd
REQUIRED_PACKAGES += library/lz4
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += web/curl
