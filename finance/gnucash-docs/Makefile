# $NetBSD: Makefile,v 1.50 2021/06/28 07:35:17 wiz Exp $

DISTNAME=		gnucash-docs-4.6
CATEGORIES=		finance
MASTER_SITES=		${MASTER_SITE_SOURCEFORGE:=gnucash/}

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		https://www.gnucash.org/
COMMENT=		Documentation for GnuCash - personal double-entry accounting program
LICENSE=		gnu-gpl-v3 AND gnu-fdl-v1.1

DEPENDS+=		yelp-[0-9]*:../../misc/yelp3

USE_TOOLS+=		gmake
GNU_CONFIGURE=		yes

CHECK_PORTABILITY_SKIP+=	guide/*/Makefile.in
CHECK_PORTABILITY_SKIP+=	help/*/Makefile.in

.include "../../mk/bsd.pkg.mk"
