# $NetBSD: Makefile,v 1.8 2020/01/18 21:51:11 jperkin Exp $
#

DISTNAME=		siege-4.0.4
PKGREVISION=		1
CATEGORIES=		www
MASTER_SITES=		http://download.joedog.org/siege/

MAINTAINER=		nils@NetBSD.org
HOMEPAGE=		http://www.joedog.org/JoeDog/Siege
COMMENT=		Website/webserver regression testing utility
LICENSE=		gnu-gpl-v2

GNU_CONFIGURE=		yes

USE_TOOLS+=		autoconf

.include "options.mk"

BUILD_DEFS+=		VARBASE
PKG_SYSCONFSUBDIR=	siege
EGDIR=			${PREFIX}/share/examples/siege
DOCDIR=			${PREFIX}/share/doc/siege
CONF_FILES=		${EGDIR}/urls.txt ${PKG_SYSCONFDIR}/urls.txt
CONF_FILES+=		${EGDIR}/siegerc ${PKG_SYSCONFDIR}/siegerc

SUBST_CLASSES+=		siege
SUBST_STAGE.siege=	pre-configure
SUBST_FILES.siege=	doc/Makefile.am doc/Makefile.in
SUBST_VARS.siege=	EGDIR

CONFIGURE_ARGS+=	--sysconfdir=${PKG_SYSCONFDIR}
CONFIGURE_ARGS+=	--localstatedir=${VARBASE}/log/
CONFIGURE_ENV+=		PERL=${PERL5:Q}

INSTALLATION_DIRS+=	${EGDIR} ${DOCDIR}
INSTALL_MAKE_FLAGS+=	sysconfdir=${EGDIR:Q}
NOT_FOR_PLATFORM+=	SunOS-*-*

pre-configure:
	cd ${WRKSRC} && autoconf

post-install:
	${INSTALL_DATA} ${WRKSRC}/AUTHORS ${DESTDIR}${DOCDIR}/AUTHORS
	${INSTALL_DATA} ${WRKSRC}/COPYING ${DESTDIR}${DOCDIR}/COPYING
	${INSTALL_DATA} ${WRKSRC}/ChangeLog ${DESTDIR}${DOCDIR}/ChangeLog
	${INSTALL_DATA} ${WRKSRC}/INSTALL ${DESTDIR}${DOCDIR}/INSTALL
	${INSTALL_DATA} ${WRKSRC}/PLATFORM ${DESTDIR}${DOCDIR}/PLATFORM
	${INSTALL_DATA} ${WRKSRC}/README.md ${DESTDIR}${DOCDIR}/README.md

.include "../../mk/bsd.pkg.mk"
