PORTNAME=	girara
PORTVERSION=	0.3.8
CATEGORIES=	x11-toolkits graphics
MASTER_SITES=	https://git.pwmt.org/pwmt/${PORTNAME}/-/archive/${DISTVERSION}/ \
		https://pwmt.org/projects/girara/download/

MAINTAINER=	madpilot@FreeBSD.org
COMMENT=	GTK3 Interface Library for Zathura PDF Viewer
WWW=		https://pwmt.org/projects/girara/

USES=		compiler:c11 gnome meson pathfix pkgconfig tar:xz
USE_GNOME=	cairo gdkpixbuf2 glib20 gtk30
USE_LDCONFIG=	yes

PATHFIX_MAKEFILEIN=	Makefile
LIBDIR=			${PREFIX}/lib

OPTIONS_DEFINE=		JSON NLS NOTIFY
OPTIONS_DEFAULT=	NOTIFY
JSON_DESC=		Support json configuration dump

OPTIONS_SUB=		yes

JSON_LIB_DEPENDS=	libjson-glib-1.0.so:devel/json-glib
JSON_MESON_ENABLED=	json

NLS_USES=		gettext

NOTIFY_LIB_DEPENDS=	libnotify.so:devel/libnotify
NOTIFY_MESON_ENABLED=	notify

post-patch-NLS-off: .SILENT
	${REINPLACE_CMD} -e "/subdir('po')/d" \
		${WRKSRC}/meson.build

.include <bsd.port.mk>
