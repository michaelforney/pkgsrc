# $NetBSD: Makefile,v 1.28 2020/03/10 22:09:38 wiz Exp $

DISTNAME=	poxml-${KAPPSVER}
PKGREVISION=	2
CATEGORIES=	devel

HOMEPAGE=	https://kde.org/applications/development/
COMMENT=	Translates DocBook XML files using gettext po files
LICENSE=	gnu-gpl-v2 AND gnu-fdl-v1.2

.include "../../meta-pkgs/kde/applications.mk"

BUILD_DEPENDS+=	kdoctools>=5.19.0:../../devel/kdoctools

USE_TOOLS+=	msgmerge

.include "../../devel/gettext-tools/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
