# $FreeBSD$

PORTNAME=	llfuse
PORTVERSION=	0.40
PORTREVISION=	1
CATEGORIES=	devel
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
EXTRACT_SUFX=	.tar.bz2
#DISTNAME=	${PORTNAME}-${PORTVERSION}.tar.bz2

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Python bindings for the low-level FUSE API

LICENSE=	LGPL20

USES=		python pkgconfig
USE_PYTHON=	concurrent distutils autoplist

post-install:
	${STRIP_CMD} ${STAGEDIR}${PYTHON_SITELIBDIR}/${PORTNAME}/capi.so

.include <bsd.port.mk>
