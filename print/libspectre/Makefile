# $NetBSD: Makefile,v 1.41 2020/03/10 22:08:58 wiz Exp $

DISTNAME=	libspectre-0.2.8
PKGREVISION=	12
CATEGORIES=	print
MASTER_SITES=	http://libspectre.freedesktop.org/releases/

MAINTAINER=	markd@NetBSD.org
HOMEPAGE=	https://www.freedesktop.org/wiki/Software/libspectre/
COMMENT=	Small library for rendering Postscript documents
LICENSE=	gnu-gpl-v2

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes

PKGCONFIG_OVERRIDE+=	libspectre.pc.in

.include "../../print/ghostscript/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
