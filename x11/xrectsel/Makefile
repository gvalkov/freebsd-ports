# $FreeBSD$

PORTNAME=	xrectsel
PORTVERSION=	0.1.1
PORTREVISION=	1
CATEGORIES=	x11

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Rectangle selection tool for X11

LICENSE=	BSD3CLAUSE

USE_XORG=	x11
USES=		gmake pkgconfig
PLIST_FILES=	bin/xrectsel # man/man1/xrectsel.1.gz

USE_GITHUB=	yes
GH_ACCOUNT=	gvalkov
GH_TAGNAME=	v${PORTVERSION}

WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}
MAKEFILE=	GNUmakefile
MAKE_ENV=	DESTDIR="${STAGEDIR}/${PREFIX}/"
#NO_PACKAGE=ignores cflags

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/xrectsel ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
