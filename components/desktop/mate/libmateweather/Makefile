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
# Copyright 2020 Michal Nowak
# Copyright (c) 2021 Tim Mooney.  All rights reserved
# Copyright 2022 Andreas Wacknitz
#

MATE_CATEGORY= LIB
BUILD_STYLE= configure
include ../../../../make-rules/shared-macros.mk
include $(WS_MAKE_RULES)/mate.mk

COMPONENT_NAME=		libmateweather
COMPONENT_MJR_VERSION=	1.28
COMPONENT_MNR_VERSION=	0
COMPONENT_SUMMARY=	Library to accessing online weather information
COMPONENT_ARCHIVE_HASH=	sha256:554373deb5b393b9d84b275dd2ca66c9a4a2d0e6ec92044fab8aa53e3032d2b5
COMPONENT_LICENSE=	GPLv2, LGPLv2, FDLv1.1

include $(WS_MAKE_RULES)/common.mk

# Auto-generated dependencies
REQUIRED_PACKAGES += library/desktop/gdk-pixbuf
REQUIRED_PACKAGES += library/desktop/gtk3
REQUIRED_PACKAGES += library/glib2
REQUIRED_PACKAGES += library/libsoup
REQUIRED_PACKAGES += library/libxml2
REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/math
