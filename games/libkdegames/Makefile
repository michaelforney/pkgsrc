# $NetBSD: Makefile,v 1.38 2020/03/10 22:08:47 wiz Exp $

DISTNAME=	libkdegames-${KAPPSVER}
PKGREVISION=	2
CATEGORIES=	games

HOMEPAGE=	https://www.kde.org/applications/games/
COMMENT=	Common code and data for many KDE games
LICENSE=	gnu-lgpl-v2 AND gnu-gpl-v2 AND gnu-fdl-v1.2

.include "../../meta-pkgs/kde/applications.mk"

USE_TOOLS+=	msgmerge

.include "../../audio/libsndfile/buildlink3.mk"
.include "../../devel/kdeclarative/buildlink3.mk"
.include "../../net/kdnssd/buildlink3.mk"
.include "../../net/knewstuff/buildlink3.mk"
.include "../../x11/qt5-qtbase/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
