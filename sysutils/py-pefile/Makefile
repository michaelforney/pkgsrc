# $NetBSD: Makefile,v 1.11 2019/11/04 21:28:51 rillig Exp $

PEFILE_VERSION=	1.2.10-139
DISTNAME=	pefile-${PEFILE_VERSION}
PKGNAME=	${PYPKGPREFIX}-pefile-${PEFILE_VERSION:S/-/./}
CATEGORIES=	sysutils
MASTER_SITES=	https://pefile.googlecode.com/files/

MAINTAINER=	khorben@defora.org
HOMEPAGE=	https://github.com/erocarrera/pefile
COMMENT=	Python module to read and work with PE files
LICENSE=	modified-bsd

PYTHON_VERSIONS_ACCEPTED=	27

EGG_NAME=	pefile-${PEFILE_VERSION:S/-/.post/}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
