PORTNAME=	octave-forge-ltfat
PORTVERSION=	2.3.1
PORTREVISION=	12
PORTEPOCH=	1
CATEGORIES=	math
MASTER_SITES=	SF/octave/Octave%20Forge%20Packages/Individual%20Package%20Releases
DISTNAME=	${OCTAVE_PKGNAME}-${DISTVERSIONFULL}

MAINTAINER=	stephen@FreeBSD.org
COMMENT=	Octave-forge package ${OCTAVE_PKGNAME}
WWW=		https://packages.octave.org/

LICENSE=	GPLv3
LICENSE_FILE=	${WRKDIR}/${OCTAVE_SRC}/COPYING

BROKEN_FreeBSD_12_powerpc64=	fails to compile: modules/libltfat/src/dgt_multi.c:47:31: 'cexpl' undeclared (first use in this function); did you mean 'cexpf'?

LIB_DEPENDS=	libfftw3.so:math/fftw3 \
		libportaudio.so:audio/portaudio \
		libopenblas.so:math/openblas

USES=		octave

OCTAVE_SRC=		${OCTAVE_PKGNAME}

GNU_CONFIGURE=	yes

post-build:
	${RM} ${WRKSRC}/Makefile ${WRKSRC}/configure
	${RM} ${WRKSRC}/../inst/DESCRIPTION
	${RM} ${WRKSRC}/../inst/ltfat/DESCRIPTION
	${RM} ${WRKSRC}/../inst/ltfat/inst/DESCRIPTION
	cd ${WRKDIR} && ${TAR} cfz ${OCTAVE_DISTNAME}.tar.gz ${OCTAVE_SRC}

.include <bsd.port.mk>
