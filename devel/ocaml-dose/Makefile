# $OpenBSD$

COMMENT =		software repository analysis in OCaml

VERSION =		3.2.2
DISTNAME =		dose3-${VERSION}
PKGNAME =		ocaml-dose-${VERSION}

CATEGORIES =		devel

HOMEPAGE =		http://dose.gforge.inria.fr/public_html/

# LGPLv3+
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =		https://gforge.inria.fr/frs/download.php/file/33677/

MODULES =		lang/ocaml

WANTLIB =		c m
BUILD_DEPENDS =		sysutils/findlib \
			lang/ocaml-camlp4 \
			devel/ounit \
			devel/cudf,-ocaml \
			devel/ocaml-extlib \
			devel/ocaml-graph \
			devel/ocaml-pcre \
			devel/cudf,-main \
			devel/ocaml-re


FAKE_FLAGS =		BINDIR=${WRKINST}/${PREFIX}/bin

USE_GMAKE =		Yes
CONFIGURE_STYLE =	gnu
CONFIGURE_ARGS =	--with-ocamlgraph --with-oUnit

ALL_TARGET =		all #doc seems broken, needs texlive_texmf-full, graphviz and hevea


post-extract:
	#rm ${WRKSRC}/doseparse/boilerplateNoRpm.ml

post-install:
	${INSTALL_MAN} ${WRKSRC}/doc/manpages/*.1 ${PREFIX}/man/man1
	${INSTALL_MAN} ${WRKSRC}/doc/manpages/*.5 ${PREFIX}/man/man5
	${INSTALL_MAN} ${WRKSRC}/doc/manpages/*.8 ${PREFIX}/man/man8
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ocaml-dose3
	${INSTALL_DATA} \
		${WRKSRC}/{CHANGES,CREDITS,README.architecture,TODO} \
		${PREFIX}/share/doc/ocaml-dose3/


.include <bsd.port.mk>
