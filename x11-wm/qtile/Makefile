# $FreeBSD$

PORTNAME=	qtile
PORTVERSION=	0.9.1
PORTREVISION=	1
CATEGORIES=	x11-wm python

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Hackable tiling window manager written and configured in Python

LICENSE=	MIT

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cairocffi>=0.6:${PORTSDIR}/x11/py-cairocffi \
		${PYTHON_PKGNAMEPREFIX}xcffib>=0.1.11:${PORTSDIR}/x11/py-xcffib \
		${PYTHON_PKGNAMEPREFIX}cffi>=0.8.2:${PORTSDIR}/devel/py-cffi \
		${PYTHON_PKGNAMEPREFIX}six>=1.4.1:${PORTSDIR}/devel/py-six

USE_GITHUB=	yes
GH_ACCOUNT=	qtile
GH_COMMIT=	da482ad
GH_TAGNAME=	v0.9.1

USES=		python
USE_PYTHON=	concurrent distutils autoplist

PORTDOCS=	CHANGELOG README.rst
OPTIONS_DEFINE=	DOCS

.include <bsd.port.options.mk>
.include <bsd.port.pre.mk>

.if ${PYTHON_VER} <= 3.3
RUN_DEPENDS+=	${PYTHON_PKGNAMEPREFIX}trollius>0:${PORTSDIR}/devel/py-trollius
.endif

post-patch:
	@${REINPLACE_CMD} -e 's|share/man/man1|man/man1|g' ${WRKSRC}/setup.py

post-install:
.if ${PORT_OPTIONS:MDOCS}
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S,^,${WRKSRC}/,} ${STAGEDIR}${DOCSDIR}
.endif

.include <bsd.port.post.mk>
