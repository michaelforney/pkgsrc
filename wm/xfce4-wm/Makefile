# $NetBSD: Makefile,v 1.77 2020/03/10 22:11:08 wiz Exp $

PKGREVISION= 2
.include "../../meta-pkgs/xfce4/Makefile.common"

VERSION=	4.14.0
DISTNAME=	xfwm4-${VERSION}
PKGNAME=	xfce4-wm-${VERSION}
CATEGORIES=	wm
MASTER_SITES+=	http://archive.xfce.org/src/xfce/xfwm4/${VERSION:R}/

HOMEPAGE=	https://docs.xfce.org/xfce/xfwm4/start
COMMENT=	XFCE window manager

.include "../../devel/libwnck3/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../x11/gtk3/buildlink3.mk"
.include "../../x11/libXdamage/buildlink3.mk"
.include "../../x11/libXfixes/buildlink3.mk"
.include "../../x11/libXpresent/buildlink3.mk"
.include "../../x11/libxfce4ui/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
