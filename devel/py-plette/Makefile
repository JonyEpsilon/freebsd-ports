PORTNAME=	plette
PORTVERSION=	0.4.2
CATEGORIES=	devel python
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Structured Pipfile and Pipfile.lock models
WWW=		https://github.com/sarugaku/plette

LICENSE=	ISCL
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}tomlkit>=0:textproc/py-tomlkit@${PY_FLAVOR}

USES=		python:3.7+
USE_PYTHON=	autoplist concurrent distutils

NO_ARCH=	yes

OPTIONS_DEFINE=	VALIDATION
OPTIONS_DEFAULT=VALIDATION
VALIDATION_DESC=Validation support

VALIDATION_RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}Cerberus>=0:devel/py-cerberus@${PY_FLAVOR}

.include <bsd.port.mk>
