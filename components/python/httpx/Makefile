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
#   $WS_TOOLS/python-integrate-project httpx
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		httpx
HUMAN_VERSION =			0.27.0
COMPONENT_SUMMARY =		httpx - The next generation HTTP client.
COMPONENT_PROJECT_URL =		https://github.com/encode/httpx
COMPONENT_ARCHIVE_URL =		\
	https://github.com/encode/httpx/archive/refs/tags/$(HUMAN_VERSION).tar.gz
COMPONENT_ARCHIVE_HASH =	\
	sha256:b7ad539016912567002a5358ad8f0dbf5873d963467f9bd2af6ba37eddc13c6e
COMPONENT_LICENSE =		BSD-3-Clause
COMPONENT_LICENSE_FILE =	LICENSE.md

TEST_STYLE = pytest

include $(WS_MAKE_RULES)/common.mk

# Random temporary directory name
# see also https://github.com/encode/httpx/discussions/3016
COMPONENT_TEST_TRANSFORMS += "-e '/\/tmp\/.*garbage/d'"

# This project does not support tox so we need to provide test requirements
# manually.
TEST_REQUIREMENTS += requirements.txt

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/anyio
PYTHON_REQUIRED_PACKAGES += library/python/certifi
PYTHON_REQUIRED_PACKAGES += library/python/hatch-fancy-pypi-readme
PYTHON_REQUIRED_PACKAGES += library/python/hatchling
PYTHON_REQUIRED_PACKAGES += library/python/httpcore
PYTHON_REQUIRED_PACKAGES += library/python/idna
PYTHON_REQUIRED_PACKAGES += library/python/sniffio
PYTHON_REQUIRED_PACKAGES += runtime/python
TEST_REQUIRED_PACKAGES.python += library/python/chardet
TEST_REQUIRED_PACKAGES.python += library/python/coverage
TEST_REQUIRED_PACKAGES.python += library/python/cryptography
TEST_REQUIRED_PACKAGES.python += library/python/mypy
TEST_REQUIRED_PACKAGES.python += library/python/pytest
TEST_REQUIRED_PACKAGES.python += library/python/socksio
TEST_REQUIRED_PACKAGES.python += library/python/tomli
TEST_REQUIRED_PACKAGES.python += library/python/trustme
TEST_REQUIRED_PACKAGES.python += library/python/uvicorn
