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
#   $WS_TOOLS/python-integrate-project Cython
#

BUILD_STYLE = setup.py

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		Cython
HUMAN_VERSION =			3.0.10
COMPONENT_SUMMARY =		Cython - The Cython compiler for writing C extensions in the Python language.
COMPONENT_PROJECT_URL =		https://cython.org/
COMPONENT_ARCHIVE_HASH =	\
	sha256:dcc96739331fb854dcf503f94607576cfe8488066c61ca50dfd55836f132de99
COMPONENT_LICENSE =		Apache-2.0
COMPONENT_LICENSE_FILE =	LICENSE.txt

include $(WS_MAKE_RULES)/common.mk

# Use well known path for Cython cache directory
COMPONENT_TEST_ENV += CYTHON_CACHE_DIR=$(@D)/.cython-cache-dir
# Testing installs packages using pip so direct it to private directory
COMPONENT_TEST_ENV += PYTHONUSERBASE=$(@D)/.python-user-base

# Normalize tmp dir name
COMPONENT_TEST_TRANSFORMS += "-e 's|\(TEST_TMP/cycache-test\).\{8\}\(/src\).\{8\}/|\1\2/|g'"
COMPONENT_TEST_TRANSFORMS += "-e 's|\(TEST_TMP/recythonize-test\).\{8\}\(/src\).\{8\}/|\1\2/|g'"
# Normalize pointer
COMPONENT_TEST_TRANSFORMS += "-e 's/\(Broken object at \)0x[a-f0-9]\{1,\}>/\1\$$(POINTER)>/g'"
# Remove line with private path
COMPONENT_TEST_TRANSFORMS += "-e '/^libgcov profiling error:/d'"
# Remove profiling info
COMPONENT_TEST_TRANSFORMS += "-e '/^Most expensive pipeline stages:/d'"

# https://github.com/OpenIndiana/oi-userland/pull/16549#issuecomment-2037519250
TEST_CONFLICTING_PACKAGES.python += library/python/numpy

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/importlib-metadata
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += runtime/python
REQUIRED_PACKAGES += system/library
