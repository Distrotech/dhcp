AM_CPPFLAGS = -DLOCALSTATEDIR='"@localstatedir@"'

sbin_PROGRAMS = dhcrelay
dhcrelay_SOURCES = dhcrelay.c
dhcrelay_LDADD = ../common/libdhcp.a ../omapip/libomapi.a \
		 $(EXPORT_DIR)/libdns.a $(EXPORT_DIR)/libisc.a \
		 -lgssapi_krb5 -lkrb5 -lgss -lcrypto
man_MANS = dhcrelay.8
EXTRA_DIST = $(man_MANS)

