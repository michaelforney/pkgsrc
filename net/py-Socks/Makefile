# $NetBSD: Makefile,v 1.6 2019/12/11 14:49:15 adam Exp $

DISTNAME=	PySocks-1.7.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/Py//}
CATEGORIES=	net python
MASTER_SITES=	${MASTER_SITE_PYPI:=P/PySocks/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/Anorov/PySocks
COMMENT=	Python SOCKS client module
LICENSE=	modified-bsd

CONFLICTS=	${PYPKGPREFIX}-SocksiPy-branch-[0-9]*

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
