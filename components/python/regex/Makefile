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
# This file was automatically generated using the following command:
#   $WS_TOOLS/python-integrate-project regex
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		regex
HUMAN_VERSION =			2024.5.15
COMPONENT_SUMMARY =		Alternative regular expression module, to replace re.
COMPONENT_PROJECT_URL =		https://github.com/mrabarnett/mrab-regex
COMPONENT_ARCHIVE_HASH =	\
	sha256:d3ee02d9e5f482cc8309134a91eeaacbdd2261ba111b0fef3748eeb4913e6a2c
COMPONENT_LICENSE =		Apache-2.0
COMPONENT_LICENSE_FILE =	LICENSE.txt

# We need to force unittest test style because the pytest test style
# (automatically detected) fails.
# https://github.com/mrabarnett/mrab-regex/issues/416
TEST_STYLE = unittest

include $(WS_MAKE_RULES)/common.mk

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/wheel
PYTHON_REQUIRED_PACKAGES += runtime/python
REQUIRED_PACKAGES += system/library
