PORTNAME=	pyicu
PORTVERSION=	2.4.3
PORTREVISION=	5
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
DISTNAME=	PyICU-${PORTVERSION}

MAINTAINER=	bland@FreeBSD.org
COMMENT=	Python extension wrapping IBM's ICU C++ API #'
WWW=		https://pypi.org/project/PyICU/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libicudata.so:devel/icu

USES=		compiler:c++11-lang python:3.6+
USE_CXXSTD=	c++11
USE_PYTHON=	distutils autoplist

MAKE_ENV=	PYICU_INCLUDES="${LOCALBASE}/include" \
		PYICU_CFLAGS="${CXXFLAGS:ts:}" \
		PYICU_LFLAGS="-L${LOCALBASE}/lib"
CFLAGS+=	-w -DPYICU_VER=\"${PORTVERSION}\"

pre-configure:
	@if [ ! -e ${LOCALBASE}/lib/libicule.so ]; then \
		${REINPLACE_CMD} "s/, 'icule'//" ${WRKSRC}/${PYSETUP}; \
	fi

.include <bsd.port.mk>
