# $NetBSD: Makefile,v 1.4 2019/12/06 19:30:10 markd Exp $

DISTNAME=	lato
PKGNAME=	tex-${DISTNAME}-3.3
TEXLIVE_REV=	51462

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://ctan.org/pkg/lato
COMMENT=	Lato font family and LaTeX support
LICENSE=	ofl-v1.1 AND lppl-1.3c

TEX_MAP_FILES+=	lato.map

TEXLIVE_UNVERSIONED=	yes
.include "../../print/texlive/package.mk"
.include "../../mk/bsd.pkg.mk"
