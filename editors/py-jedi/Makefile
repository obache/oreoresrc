# $NetBSD: Makefile,v 1.7 2021/01/04 16:36:04 adam Exp $

DISTNAME=	jedi-0.18.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	editors python
MASTER_SITES=	${MASTER_SITE_PYPI:=j/jedi/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/davidhalter/jedi
COMMENT=	Autocompletion tool for Python that can be used for text editors
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-parso>=0.8.0:../../lang/py-parso
DEPENDS+=	${PYPKGPREFIX}-readline-[0-9]*:../../devel/py-readline
TEST_DEPENDS+=	${PYPKGPREFIX}-colorama-[0-9]*:../../comms/py-colorama
TEST_DEPENDS+=	${PYPKGPREFIX}-docopt-[0-9]*:../../devel/py-docopt

PYTHON_VERSIONED_DEPENDENCIES=	test:test

PYTHON_VERSIONS_INCOMPATIBLE=	27 # py-parso

USE_LANGUAGES=	# none

do-test:
	cd ${WRKSRC} && ${SETENV} ${MAKE_ENV} pytest-${PYVERSSUFFIX}

.include "../../lang/python/egg.mk"
.include "../../lang/python/versioned_dependencies.mk"
.include "../../mk/bsd.pkg.mk"
