# $NetBSD: Makefile,v 1.9 2020/03/26 12:07:19 nia Exp $

DISTNAME=	buzztrax-0.10.2
PKGREVISION=	2
CATEGORIES=	audio
MASTER_SITES=	https://files.buzztrax.org/releases/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://buzztrax.org/
COMMENT=	Modular, free, open source music studio
LICENSE=	gnu-lgpl-v2.1

TOOL_DEPENDS+=	libxslt-[0-9]*:../../textproc/libxslt
DEPENDS+=	gsettings-desktop-schemas-[0-9]*:../../sysutils/gsettings-desktop-schemas

CONFLICTS+=	buzztard-[0-9]*
SUPERSEDES+=	buzztard-[0-9]*

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes
USE_LANGUAGES=	c c++

USE_TOOLS+=	intltool perl pkg-config
USE_TOOLS+=	msgfmt msgmerge xgettext
USE_TOOLS+=	gmake

# GLib-GIO-ERROR **: Settings schema 'org.buzztrax' is not installed
MAKE_ENV+=	GCONF_DISABLE_MAKEFILE_SCHEMA_INSTALL=1

PLIST_SRC=	${PLIST_SRC_DFLT}

USE_PKGLOCALEDIR=	yes

CONFIGURE_ARGS+=	--disable-dllwrapper
CONFIGURE_ARGS+=	--disable-schemas-compile

.include "options.mk"
.include "../../devel/glib2/schemas.mk"
.include "../../graphics/clutter-gtk/buildlink3.mk"
.include "../../graphics/gnome-icon-theme/buildlink3.mk"
.include "../../graphics/hicolor-icon-theme/buildlink3.mk"
.include "../../multimedia/gstreamer1/buildlink3.mk"
.include "../../multimedia/gst-plugins1-base/buildlink3.mk"
.include "../../textproc/aspell/buildlink3.mk"
.include "../../textproc/libxml2/buildlink3.mk"
.include "../../sysutils/desktop-file-utils/desktopdb.mk"
.include "../../x11/gtk3/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
