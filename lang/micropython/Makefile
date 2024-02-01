PORTNAME=	micropython
PORTVERSION=	1.20
DISTVERSIONPREFIX=	v
PORTREVISION=	2
CATEGORIES=	lang python

MAINTAINER=	Duncan.Lowther@glasgow.ac.uk
COMMENT=	Implementation of the Python language for microcontrollers
WWW=		https://www.micropython.org/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libffi.so:devel/libffi

USES=		gmake pkgconfig python:,build

BINARY_ALIAS=	python3=${PYTHON_CMD}

USE_GITHUB=     yes
GH_ACCOUNT?=    glasgowPLI
GH_PROJECT?=    micropython
GH_TAGNAME?=    6035f726a173029936914635dc8aad8610d2966b

BUILD_WRKSRC=	${WRKSRC}/ports/unix
TEST_WRKSRC=	${WRKSRC}/ports/unix

PLIST_FILES=	bin/micropython

do-install:
	${INSTALL_PROGRAM} ${BUILD_WRKSRC}/micropython ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
