#	From: @(#)Makefile	8.1 (Berkeley) 6/6/93
# $FreeBSD$

.PATH: ${.CURDIR:H}/common_source

PROG=	lpc
MAN=	lpc.8
SRCS=	lpc.c cmds.c cmdtab.c movejobs.c 
BINGRP=	daemon
BINMODE= 2555

CFLAGS+= -I${.CURDIR:H}/common_source

WARNS?=	0

DPADD=	${LIBLPR} ${LIBEDIT} ${LIBTERMCAP}
LDADD=	${LIBLPR} -ledit -ltermcap

.include <bsd.prog.mk>
