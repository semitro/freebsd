# $FreeBSD$

.include <bsd.own.mk>

NETBSD_ATF_TESTS_C=

.if ${MK_OPENSSL} != "no"
# XXX: doesn't compile
#NETBSD_ATF_TESTS_C+=	hmac_test
NETBSD_ATF_TESTS_C+=	sha2_test
.endif

NETBSD_ATF_TESTS_SH=	hash_test

BINDIR=		${TESTSDIR}

PROGS+=		h_hash

FILESDIR=	${TESTSDIR}/data

FILES+=		data/md5test-in
FILES+=		data/md5test-out
FILES+=		data/sha1test-in
FILES+=		data/sha1test-out
FILES+=		data/sha1test2-out

DPADD+=		${LIBMD}
LDADD+=		-lmd
DPADD.sha2_test+=	${LIBCRYPTO}
LDADD.sha2_test+=	-lcrypto

CFLAGS.h_hash+=		-I${SRCTOP}/lib/libnetbsd

.include "../Makefile.netbsd-tests"

.include <bsd.test.mk>
