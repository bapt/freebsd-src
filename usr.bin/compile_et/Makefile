.PATH: ${SRCTOP}/contrib/com_err

PACKAGE=	kerberos

PROG=	compile_et
SRCS=	compile_et.c parse.y lex.l
.if defined(BOOTSTRAPPING)
LIBROKEN_A=	${.OBJDIR:H:H}/kerberos5/lib/libroken/libroken.a
LDADD=	${LIBROKEN_A}
DPADD=	${LIBROKEN_A}
.else
LIBADD=	roken
.endif
LIBADD+=	vers
CFLAGS+=-I. -I${SRCTOP}/contrib/com_err

WARNS?=	0

.include <bsd.prog.mk>
