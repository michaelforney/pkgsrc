# $NetBSD: Makefile,v 1.23 2020/03/26 21:51:49 joerg Exp $
#

DISTNAME=	darkice-1.2
CATEGORIES=	audio
MASTER_SITES=	https://darkice.googlecode.com/files/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://darkice.tyrell.hu/
COMMENT=	IceCast, IceCast2 and ShoutCast live audio streamer
LICENSE=	gnu-gpl-v3

GNU_CONFIGURE=		yes
USE_LANGUAGES=		c c++
USE_TOOLS+=		gmake

CHECK_PORTABILITY_SKIP+=	configure.in

CONFIGURE_ARGS+=	--with-vorbis-prefix=${BUILDLINK_PREFIX.libvorbis}
CONFIGURE_ARGS+=	--with-lame-prefix=${BUILDLINK_PREFIX.lame}
CONFIGURE_ARGS+=	--with-twolame-prefix=${BUILDLINK_PREFIX.twolame}
CONFIGURE_ARGS+=	--with-faac-prefix=${BUILDLINK_PREFIX.faac}
CONFIGURE_ARGS+=	--without-jack
LIBS+=			${LIBOSSAUDIO:Q}

EGDIR=		${PREFIX}/share/examples/darkice
HTMLDIR=	${PREFIX}/share/doc/darkice

CONF_FILES=	${EGDIR}/darkice.conf ${PKG_SYSCONFDIR}/darkice.conf

INSTALLATION_DIRS=	bin ${PKGMANDIR}/man1 ${PKGMANDIR}/man5

do-install:
	${INSTALL_DATA_DIR} ${DESTDIR}${EGDIR}
	${INSTALL_DATA_DIR} ${DESTDIR}${HTMLDIR}
	${INSTALL_DATA} ${WRKSRC}/darkice.cfg \
		${DESTDIR}${EGDIR}/darkice.conf
	${INSTALL_PROGRAM} ${WRKSRC}/src/darkice ${DESTDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/man/darkice.1 \
		${DESTDIR}${PREFIX}/${PKGMANDIR}/man1
	${INSTALL_MAN} ${WRKSRC}/man/darkice.cfg.5 \
		${DESTDIR}${PREFIX}/${PKGMANDIR}/man5/darkice.conf.5

.include "../../audio/faac/buildlink3.mk"
.include "../../audio/lame/buildlink3.mk"
.include "../../audio/libvorbis/buildlink3.mk"
.include "../../audio/twolame/buildlink3.mk"

.include "../../mk/pthread.buildlink3.mk"
.include "../../mk/oss.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
