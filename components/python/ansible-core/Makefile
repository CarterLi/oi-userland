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
#   $WS_TOOLS/python-integrate-project -d python/ansible-core ansible_core
#

BUILD_STYLE = pyproject

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME =		ansible_core
HUMAN_VERSION =			2.15.12
COMPONENT_SUMMARY =		Radically simple IT automation
COMPONENT_PROJECT_URL =		https://ansible.com/
COMPONENT_ARCHIVE_HASH =	\
	sha256:5fde82cd3928d9857ad880782c644f27d3168b0f25321d5a8d6befa524aa1818
COMPONENT_LICENSE =		GPL-3.0-only
COMPONENT_LICENSE_FILE =	COPYING

# ansible-core >= 2.14.0 requires Python >= 3.9
UNSUPPORTED_PYTHON_VERSIONS =
PYTHON_VERSIONS := $(filter-out $(UNSUPPORTED_PYTHON_VERSIONS), $(PYTHON_VERSIONS))

# ansible-core use custom testing (see below)
TEST_STYLE = custom

include $(WS_MAKE_RULES)/common.mk

# Make sure the unversioned generic package depends on unsupported versioned package(s) too.
$(BUILD_DIR)/mkgeneric-python:	PYTHON_VERSIONS := $(UNSUPPORTED_PYTHON_VERSIONS) $(PYTHON_VERSIONS)

# custom testing
# https://docs.ansible.com/ansible/latest/dev_guide/testing_running_locally.html#testing-ansible-core
COMPONENT_TEST_CMD = bin/ansible-test
COMPONENT_TEST_ARGS =
COMPONENT_TEST_ARGS += units
COMPONENT_TEST_ARGS += --python $(PYTHON_VERSION)
COMPONENT_TEST_ARGS += --python-interpreter $(PYTHON)
COMPONENT_TEST_ARGS += --local
COMPONENT_TEST_ARGS += --color no
COMPONENT_TEST_ARGS += --verbose
COMPONENT_TEST_TARGETS =

# This project does not support tox so we need to provide test requirements
# manually.
TEST_REQUIREMENTS += test/lib/ansible_test/_data/requirements/units.txt

# testing fails without HOME environment variable
COMPONENT_TEST_ENV += HOME=/tmp

# The ansible-test is running pytest several times in a row with pytest-xdist
# plugin enabled.  This is hard to normalize properly, so we just pick most
# important lines from the test log and normalize them.
COMPONENT_TEST_TRANSFORMS = \
	"-n -e '/^\[gw/p' \
	| $(COMPONENT_TEST_TRANSFORMER) \
		-e 's/^\[gw.\] \[...%\] //' \
		-e 's/\([^ ]\{1,\}\) \(.*\)$$/\2 \1/' \
		-e 's/\(test_distribution_version\[stdin\)[0-9]*/\1/' \
		-e 's|$(@D)|\$$(@D)|g' \
	| $(SORT) \
	| $(COMPONENT_TEST_TRANSFORMER) -e ''"

# Auto-generated dependencies
PYTHON_REQUIRED_PACKAGES += library/python/cryptography
PYTHON_REQUIRED_PACKAGES += library/python/importlib-resources
PYTHON_REQUIRED_PACKAGES += library/python/jinja2
PYTHON_REQUIRED_PACKAGES += library/python/packaging
PYTHON_REQUIRED_PACKAGES += library/python/pyyaml
PYTHON_REQUIRED_PACKAGES += library/python/resolvelib
PYTHON_REQUIRED_PACKAGES += library/python/setuptools
PYTHON_REQUIRED_PACKAGES += library/python/wheel
PYTHON_REQUIRED_PACKAGES += runtime/python
TEST_REQUIRED_PACKAGES.python += library/python/mock
TEST_REQUIRED_PACKAGES.python += library/python/pytest
TEST_REQUIRED_PACKAGES.python += library/python/pytest-forked
TEST_REQUIRED_PACKAGES.python += library/python/pytest-mock
TEST_REQUIRED_PACKAGES.python += library/python/pytest-xdist
TEST_REQUIRED_PACKAGES.python += library/python/pyyaml
