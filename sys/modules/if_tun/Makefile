# $FreeBSD$

.PATH: ${.CURDIR}/../../net

KMOD=	if_tun
SRCS=	if_tun.c opt_inet.h opt_inet6.h

.if !defined(KERNBUILDDIR)
opt_inet.h:
	echo "#define INET 1" > ${.TARGET}

opt_inet6.h:
	echo "#define INET6 1" > ${.TARGET}
.endif

.include <bsd.kmod.mk>
