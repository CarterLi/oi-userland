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
#   $WS_TOOLS/python-integrate-project domdf_python_tools
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		domdf_python_tools
HUMAN_VERSION =			3.9.0
COMPONENT_SUMMARY =		Helpful functions for Python
COMPONENT_PROJECT_URL =		https://github.com/domdfcoding/domdf_python_tools
COMPONENT_ARCHIVE_HASH =	\
	sha256:1f8a96971178333a55e083e35610d7688cd7620ad2b99790164e1fc1a3614c18
COMPONENT_LICENSE =		MIT
COMPONENT_LICENSE_FILE =	LICENSE

TEST_STYLE = setup.py

#
# Following dependency loops were detected (where 'A --> B' means 'A needs B to
# run tests', and 'A ==> B' means 'A needs B for build and/or run'):
#
# domdf_python_tools --> coincidence ==> whey ==> domdf_python_tools
#
# To break loops we need to allow this project to integrate without testing in
# a case the required projects are not available yet (bootstrap).
#
PYTHON_TEST_BOOTSTRAP = yes

include $(WS_MAKE_RULES)/common.mk

# https://github.com/domdfcoding/domdf_python_tools/issues/114
TEST_REQUIRED_PACKAGES.python += library/python/coincidence

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/natsort
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/typing-extensions
PYTHON_REQUIRED_PACKAGES += library/python/wheel
PYTHON_REQUIRED_PACKAGES += runtime/python
