# $NetBSD: Makefile,v 1.17 2020/01/10 09:28:41 nros Exp $

DISTNAME=	googletest-1.8.1
PKGREVISION=	1
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=google/}
GITHUB_TAG=	release-${PKGVERSION_NOREV}

MAINTAINER=	reed@reedmedia.net
HOMEPAGE=	https://github.com/google/googletest
COMMENT=	Google's C++ testing framework
LICENSE=	modified-bsd

INSTALLATION_DIRS=	bin

USE_CMAKE=		yes
USE_LANGUAGES=		c c++11

PKGCONFIG_OVERRIDE+=	googlemock/cmake/gmock.pc.in
PKGCONFIG_OVERRIDE+=	googlemock/cmake/gmock_main.pc.in
PKGCONFIG_OVERRIDE+=	googletest/cmake/gtest.pc.in
PKGCONFIG_OVERRIDE+=	googletest/cmake/gtest_main.pc.in

.include "../../mk/bsd.pkg.mk"
