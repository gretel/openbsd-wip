# $OpenBSD$

COMMENT =		universal vector graphics translator

V = 			1.1.5
DISTNAME =		uniconvertor-${V}

CATEGORIES =		graphics

HOMEPAGE =		http://sk1project.org/

MAINTAINER =		Kirill Bychkov <yason@linklevel.net>

# GPLv2/LGPLv2
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =		https://uniconvertor.googlecode.com/files/

MODULES =		lang/python

NO_TEST =		Yes

SEPARATE_BUILD = 	concurrent

SUBST_VARS = 		V
MODPY_ADJ_FILES = 	setup.py src/uniconv src/__init__.py

.include <bsd.port.mk>
