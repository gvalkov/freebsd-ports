# $FreeBSD$

PORTNAME=	slop
PORTVERSION=	3.1.14
PORTREVISION=	1
CATEGORIES=	x11

MAINTAINER=	georgi.t.valkov@gmail.com
COMMENT=	Rectangle selection tool for X11

LICENSE=	GPLv3

BUILD_DEPENDS=	gsed:${PORTSDIR}/textproc/gsed \
		gengetopt:${PORTSDIR}/devel/gengetopt

USE_XORG=	x11
USES=		cmake:outsource
PLIST_FILES=	bin/slop

CMAKE_VERBOSE = yes
USE_GITHUB=	yes
GH_ACCOUNT=	naelstrof
GH_COMMIT=	ce9a0ca
GH_TAGNAME=	${GH_COMMIT}

WRKSRC=		${WRKDIR}/${GH_ACCOUNT}-${PORTNAME}-${GH_COMMIT}

post-patch:
	@${REINPLACE_CMD} -e 's,"/usr/bin","${PREFIX}/bin",g' ${WRKSRC}/CMakeLists.txt

.include <bsd.port.mk>
