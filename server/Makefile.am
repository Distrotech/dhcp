AM_CPPFLAGS = -I.. -DLOCALSTATEDIR='"@localstatedir@"'

dist_sysconf_DATA = dhcpd.conf
sbin_PROGRAMS = dhcpd
dhcpd_SOURCES = dhcpd.c dhcp.c bootp.c confpars.c db.c class.c failover.c \
		omapi.c mdb.c stables.c salloc.c ddns.c dhcpleasequery.c \
		dhcpv6.c mdb6.c ldap.c ldap_casa.c

dhcpd_CFLAGS = $(LDAP_CFLAGS)
dhcpd_LDADD = ../common/libdhcp.a ../omapip/libomapi.a \
	      ../dhcpctl/libdhcpctl.a \
	      $(EXPORT_DIR)/libdns.a $(EXPORT_DIR)/libisc.a \
	      -lgssapi_krb5 -lkrb5 -lgss -lcrypto

man_MANS = dhcpd.8 dhcpd.conf.5 dhcpd.leases.5
EXTRA_DIST = $(man_MANS)

