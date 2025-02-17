PORTNAME=	xfce4-conf
PORTVERSION=	4.18.0
CATEGORIES=	x11 xfce
MASTER_SITES=	XFCE
DISTNAME=	xfconf-${DISTVERSIONFULL}
DIST_SUBDIR=	xfce4

MAINTAINER=	xfce@FreeBSD.org
COMMENT=	D-Bus-based configuration storage system
WWW=		https://www.xfce.org/projects

LICENSE=	GPLv2

BUILD_DEPENDS=	p5-XML-Parser>=2.44:textproc/p5-XML-Parser

USES=		compiler:c11 gettext-tools gmake gnome libtool pathfix perl5 \
		pkgconfig tar:bzip2 xfce xorg
USE_GNOME=	glib20 intltool
USE_LDCONFIG=	yes
USE_PERL5=	build
USE_XFCE=	libutil
USE_XORG=	x11

GNU_CONFIGURE=	yes
INSTALL_TARGET=	install-strip
CONFIGURE_ARGS=	--without-html-dir \
		--without-bash-completion-dir

PORTSCOUT=	limitw:1,even

OPTIONS_DEFINE=		GIR NLS VAPI
OPTIONS_DEFAULT=	GIR VAPI
OPTIONS_SUB=		yes

GIR_DESC=		Use Gobject Introspection

GIR_USE=		gnome=introspection:build
GIR_CONFIGURE_ON=	--enable-introspection=yes
GIR_CONFIGURE_OFF=	--enable-introspection=no

NLS_CONFIGURE_ENABLE=	nls
NLS_USES=		gettext-runtime

VAPI_USES=		vala:build
VAPI_CONFIGURE_ENABLE=	vala
VAPI_IMPLIES=		GIR

.include <bsd.port.mk>
