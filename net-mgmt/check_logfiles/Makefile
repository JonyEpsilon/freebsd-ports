PORTNAME=	check_logfiles
PORTVERSION=	4.1.0.1
CATEGORIES=	net-mgmt
MASTER_SITES=	https://labs.consol.de/assets/downloads/nagios/

MAINTAINER=	flo@FreeBSD.org
COMMENT=	Nagios plugin which scans log files for specific patterns
WWW=		https://labs.consol.de/lang/en/nagios/check_logfiles/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

PLIST_FILES=	libexec/nagios/check_logfiles

USES=		autoreconf gmake perl5
GNU_CONFIGURE=	yes
CONFIGURE_ARGS+=	--with-trusted-path=/bin:/sbin:/usr/bin:/usr/sbin:${LOCALBASE}/bin:${LOCALBASE}/sbin \
			--libexecdir=${PREFIX}/libexec/nagios

.include <bsd.port.mk>
