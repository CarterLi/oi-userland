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
#   $WS_TOOLS/python-integrate-project multidict
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		multidict
HUMAN_VERSION =			6.0.5
COMPONENT_SUMMARY =		multidict - multidict implementation
COMPONENT_PROJECT_URL =		https://github.com/aio-libs/multidict
COMPONENT_ARCHIVE_URL =		\
	https://files.pythonhosted.org/packages/f9/79/722ca999a3a09a63b35aac12ec27dfa8e5bb3a38b0f857f7a1a209a88836/multidict-6.0.5.tar.gz
COMPONENT_ARCHIVE_HASH =	\
	sha256:f7e301075edaf50500f0b341543c41194d8df3ae5caf4702f2095f3ca73dd8da
COMPONENT_LICENSE =		Apache-2.0
COMPONENT_LICENSE_FILE =	LICENSE

TEST_STYLE = pytest

include $(WS_MAKE_RULES)/common.mk

#
# Tests are run from build directory that contains cloned copy of sdist.  We
# try to ask Python to find tested modules in the proto area (the PYTHONPATH is
# set accordingly), but Python (< 3.11) always adds the current directory to
# sys.path and there is no known (simple) way how to avoid that.  Except -I,
# but that would cause Python to ignore PYTHONPATH too so we would not have
# access to the proto area either.  The -P option together with PYTHONSAFEPATH
# environment variable were added to Python 3.11 only so we cannot use them yet
# for all Python versions we support.
#
# Since sdist for this project contains the main module in the top-level
# directory we cannot force Python to skip it.  But, unfortunately, this module
# does not contain built dynamic libraries, so Python cannot find them while
# testing.
#
# To workaround this we rename the main module in the build directory during
# testing so Python will need to defer to PYTHONPATH.
#
COMPONENT_PRE_TEST_ACTION +=	$(MV) $(@D)/multidict $(@D)/multidict-RENAMED ;
COMPONENT_POST_TEST_ACTION +=	$(MV) $(@D)/multidict-RENAMED $(@D)/multidict ;

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/wheel
PYTHON_REQUIRED_PACKAGES += runtime/python
REQUIRED_PACKAGES += system/library
