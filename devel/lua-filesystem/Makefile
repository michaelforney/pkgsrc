# $NetBSD: Makefile,v 1.12 2020/01/18 23:30:33 rillig Exp $
#

DISTNAME=		luafilesystem-1.7.0
PKGNAME=		${DISTNAME:S/lua/${LUA_PKGPREFIX}-/}
CATEGORIES=		devel
MASTER_SITES=		${MASTER_SITE_GITHUB:=keplerproject/}
GITHUB_PROJECT=		luafilesystem
GITHUB_TAG=		v${PKGVERSION_NOREV:S/./_/g}_2

MAINTAINER=		fhajny@NetBSD.org
HOMEPAGE=		https://keplerproject.github.com/luafilesystem/
COMMENT=		File system related library for Lua
LICENSE=		mit

WRKSRC=			${WRKDIR}/luafilesystem-${PKGVERSION_NOREV:S/./_/g}_2

USE_TOOLS+=		gmake pkg-config
BUILD_TARGET=		lib

TEST_TARGET=		test

MAKE_ENV+=		LUA_CDIR=${LUA_CDIR}
MAKE_ENV+=		LUA_VERS=${LUA_VERSION_MAJOR}.${LUA_VERSION_MINOR}

.include "../../lang/lua/module.mk"
.include "../../mk/bsd.pkg.mk"
