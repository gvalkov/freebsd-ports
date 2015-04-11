# Created by: Georgi Valkov
# $FreeBSD:

PORTNAME=	scanbd
PORTVERSION=	1.4.2
PORTREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	SF/${PORTNAME}/releases
DISTNAME=       ${PORTVERSION}
DISTFILES=	${PORTNAME}-${PORTVERSION}.tgz

MAINTAINER=	georgi.valkov@gmail.com
COMMENT=	Daemon to monitor and configure scanner buttons
LICENSE=	GPLv2

USES=		libtool gmake pkgconfig pathfix
GNU_CONFIGURE=	yes
CONFIGURE_ARGS= --with-user=saned \
		--with-group=saned
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib
USE_LDCONFIG=	yes
INSTALL_TARGET=	install-strip

USERS=	saned
GROUPS=	saned

SUB_FILES+=	pkg-message

# pre-configure:
# 	@${FIND} ${WRKSRC} -name Makefile.in | ${XARGS} \
# 		${REINPLACE_CMD} -e 's|-ldl||g'

.include <bsd.port.mk>
