# $NetBSD: Makefile,v 1.14 2020/03/21 16:57:14 bsiegert Exp $

DISTNAME=	repr-0.0.0.20180921
PKGNAME=	go-${DISTNAME}
PKGREVISION=	13
MASTER_SITES=	${MASTER_SITE_GITHUB:=alecthomas/}
CATEGORIES=	devel
GITHUB_PROJECT=	repr
GITHUB_TAG=	7ed41413b4775c49ef579a96f38890b6cd5bb39d

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/alecthomas/repr
COMMENT=	Python's repr() for Go
LICENSE=	mit

GO_DIST_BASE=	repr-${GITHUB_TAG}
GO_SRCPATH=	github.com/alecthomas/repr

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
