PORTNAME=	simple_form
PORTVERSION=	5.1.0
CATEGORIES=	devel rubygems
MASTER_SITES=	RG
PKGNAMESUFFIX=	-rails61

MAINTAINER=	bofh@FreeBSD.org
COMMENT=	Forms made easy
WWW=		https://github.com/heartcombo/simple_form

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/MIT-LICENSE

RUN_DEPENDS=	rubygem-actionpack61>=5.2:www/rubygem-actionpack61 \
		rubygem-activemodel61>=5.2:databases/rubygem-activemodel61

USES=		cpe gem
CPE_VENDOR=	plataformatec
USE_RUBY=	yes

NO_ARCH=	yes

.include <bsd.port.mk>
