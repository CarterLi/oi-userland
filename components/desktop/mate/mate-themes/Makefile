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
# Copyright 2016 Till Wegmueller
# Copyright 2016 Ken Mays
# Copyright 2019 Michal Nowak
# Copyright 2020 Marco van Wieringen
# Copyright (c) 2021 Tim Mooney.  All rights reserved
# Copyright 2022 Andreas Wacknitz
#

MATE_CATEGORY= APP
BUILD_STYLE= configure
include ../../../../make-rules/shared-macros.mk
include $(WS_MAKE_RULES)/mate.mk

COMPONENT_NAME=		mate-themes
COMPONENT_VERSION=	3.22.26
COMPONENT_SUMMARY=	MATE Themes
COMPONENT_ARCHIVE_URL= https://pub.mate-desktop.org/releases/themes/3.22/$(COMPONENT_ARCHIVE)
COMPONENT_ARCHIVE_HASH= sha256:224e89d364eb3b73f1cf756d05494a98421a93cbf54349a2c85fc607eb755ed7
COMPONENT_LICENSE=	GPLv2, LGPLv2, FDLv1.1
COMPONENT_CLASSIFICATION= System/Libraries

include $(WS_MAKE_RULES)/common.mk

# build dependencies
PERL_REQUIRED_PACKAGES += runtime/perl
PERL_REQUIRED_PACKAGES += library/perl-5/xml-parser
REQUIRED_PACKAGES += library/desktop/xdg/icon-naming-utils
REQUIRED_PACKAGES += text/intltool
REQUIRED_PACKAGES += text/gnu-gettext

# Auto-generated dependencies
