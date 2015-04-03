# $FreeBSD$

PORTNAME=	rsstail
PORTVERSION=	0.3.4
PORTREVISION=	1
CATEGORIES=	www
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Command-line syndication feed monitor

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}feedparser:${PORTSDIR}/www/py-feedparser

USES=		python
USE_PYTHON=	concurrent distutils autoplist
NO_ARCH=	yes

CONFLICTS_INSTALL= rsstail
PLIST_FILES=	etc/bash_completion.d/rsstail.sh \
		share/zsh/site-functions/_rsstail

.include <bsd.port.pre.mk>
post-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/etc/bash_completion.d
	${MKDIR} ${STAGEDIR}${PREFIX}/share/zsh/site-functions
	${INSTALL_DATA} ${WRKSRC}/etc/rsstail.sh ${STAGEDIR}${PREFIX}/etc/bash_completion.d/rsstail.sh
	${INSTALL_DATA} ${WRKSRC}/etc/_rsstail   ${STAGEDIR}${PREFIX}/share/zsh/site-functions/_rsstail

.include <bsd.port.post.mk>
