PORTNAME=	hyprland-share-picker
PORTVERSION=	s20221213
CATEGORIES=	x11 wayland

MAINTAINER=	jbeich@FreeBSD.org
COMMENT=	Share picker for xdg-desktop-portal-hyprland
WWW=		https://github.com/hyprwm/xdg-desktop-portal-hyprland

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC:H}/LICENSE

FLAVORS=	qt5 qt6

USES=		compiler:c++11-lib cmake qt:5
USE_GITHUB=	yes
USE_QT=		qmake:build buildtools:build core gui wayland:run widgets
GH_ACCOUNT=	hyprwm
GH_PROJECT=	xdg-desktop-portal-hyprland
GH_TAGNAME=	101b58d
WRKSRC_SUBDIR=	${PORTNAME}
LDFLAGS+=	-Wl,--as-needed # GL
PLIST_FILES=	bin/${PORTNAME}

.if ${FLAVOR:U} == qt6
PKGNAMESUFFIX=	-${FLAVOR}
USES:=		${USES:S/qt:5/qt:6/}
USE_QT=		base wayland:run
CONFLICTS_INSTALL=	${PORTNAME}
.else
CONFLICTS_INSTALL=	${PORTNAME}-qt6
.endif

.include <bsd.port.mk>
