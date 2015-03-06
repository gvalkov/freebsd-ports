# $FreeBSD$

PORTNAME=	cairocffi
PORTVERSION=	0.6
PORTREVISION=	1
CATEGORIES=	graphics python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Python bindings for cairo based on cffi

LICENSE=	BSD3

RUN_DEPENDS=    ${PYTHON_PKGNAMEPREFIX}cffi>0:${PORTSDIR}/devel/py-cffi

USES=		python
USE_PYTHON=	concurrent distutils autoplist
USE_GNOME=	cairo

CFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

.include <bsd.port.mk>
