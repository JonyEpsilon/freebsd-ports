PORTNAME=	ffn
DISTVERSIONPREFIX=	v
DISTVERSION=	0.3.6
CATEGORIES=	finance python
#MASTER_SITES=	CHEESESHOP # no tests
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Financial functions for Python
WWW=		http://pmorissette.github.io/ffn/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

PY_DEPENDS=	${PYTHON_PKGNAMEPREFIX}decorator>=4:devel/py-decorator@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}future>=0.15:devel/py-future@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}matplotlib>=1:math/py-matplotlib@${PY_FLAVOR} \
		${PYNUMPY} \
		${PYTHON_PKGNAMEPREFIX}pandas-datareader>=0.2:math/py-pandas-datareader@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pandas>=0.19:math/py-pandas@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}scikit-learn>=0.15:science/py-scikit-learn@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}scipy>=0.15:science/py-scipy@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}tabulate>=0.7.5:devel/py-tabulate@${PY_FLAVOR}
BUILD_DEPENDS=	${PY_DEPENDS}
RUN_DEPENDS=	${PY_DEPENDS}

USES=		python:3.6+
USE_PYTHON=	distutils autoplist pytest

USE_GITHUB=	yes
GH_ACCOUNT=	pmorissette

NO_ARCH=	yes

.include <bsd.port.mk>
