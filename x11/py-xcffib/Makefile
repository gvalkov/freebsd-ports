# $FreeBSD$

PORTNAME=	xcffib
PORTVERSION=	0.2.0
PORTREVISION=	1
CATEGORIES=	x11
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Python binding to the X Window System protocol via libxcb

LICENSE=	APACHE20

LIB_DEPENDS=    libxcb.so:${PORTSDIR}/x11/libxcb
BUILD_DEPENDS=  ${PYTHON_PKGNAMEPREFIX}cffi>=0.8.2:${PORTSDIR}/devel/py-cffi \
		${PYTHON_PKGNAMEPREFIX}six>=1.4.1:${PORTSDIR}/devel/py-six \
		libxcb>=2.4:${PORTSDIR}/x11/xcb

USES=		python
USE_PYTHON=	concurrent distutils autoplist
NO_ARCH=	yes

CFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

.include <bsd.port.mk>
