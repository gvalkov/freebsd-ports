# $FreeBSD$

PORTNAME=	attic
PORTVERSION=	0.14
PORTREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	CHEESESHOP
DISTNAME=       Attic-${PORTVERSION}

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Command-line deduplicating backup program

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}msgpack:${PORTSDIR}/devel/py-msgpack

USES=		python:3.2+
USE_PYTHON=	distutils autoplist

OPTIONS_DEFINE=	FUSE
FUSE_DESC=	Allow mounting of archives as FUSE filesystems
FUSE_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}llfuse:${PORTSDIR}/devel/py-llfuse

OPTIONS_DEFAULT=	FUSE

post-install:
.for i in crypto chunker hashindex platform_freebsd
	${STRIP_CMD} ${STAGEDIR}${PYTHON_SITELIBDIR}/${PORTNAME}/${i}.so
.endfor

.include <bsd.port.mk>
