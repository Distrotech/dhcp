dist_sysconf_DATA = dhclient.conf
sbin_PROGRAMS = dhclient
dhclient_SOURCES = clparse.c dhclient.c dhc6.c \
		   scripts/bsdos scripts/freebsd scripts/linux scripts/macos \
		   scripts/netbsd scripts/nextstep scripts/openbsd \
		   scripts/solaris scripts/openwrt
dhclient_LDADD = ../common/libdhcp.a ../omapip/libomapi.a \
		 $(EXPORT_DIR)/libdns.a $(EXPORT_DIR)/libisc.a \
		 -lgssapi_krb5 -lkrb5 -lgss -lcrypto
man_MANS = dhclient.8 dhclient-script.8 dhclient.conf.5 dhclient.leases.5
EXTRA_DIST = $(man_MANS)

dhclient.o: dhclient.c
	$(COMPILE) -DCLIENT_PATH='"PATH=$(sbindir):/sbin:/bin:/usr/sbin:/usr/bin"' \
		   -DLOCALSTATEDIR='"$(localstatedir)"' -c dhclient.c

dhc6.o: dhc6.c
	$(COMPILE) -DCLIENT_PATH='"PATH=$(sbindir):/sbin:/bin:/usr/sbin:/usr/bin"' \
		   -DLOCALSTATEDIR='"$(localstatedir)"' -c dhc6.c
