# $NetBSD: Makefile,v 1.3 2019/06/16 19:12:40 adam Exp $

DISTNAME=	memory_profiler-0.55.0
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/_/-/}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=m/memory_profiler/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/pythonprofilers/memory_profiler
COMMENT=	Monitors memory usage of a Python program
LICENSE=	modified-bsd

DEPENDS+=	${PYPKGPREFIX}-matplotlib-[0-9]*:../../graphics/py-matplotlib
DEPENDS+=	${PYPKGPREFIX}-psutil-[0-9]*:../../sysutils/py-psutil

USE_LANGUAGES=	# none

PYTHON_VERSIONS_INCOMPATIBLE=	27	# py-matplotlib

post-install:
	cd ${DESTDIR}${PREFIX}/bin && \
	${MV} mprof mprof-${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
