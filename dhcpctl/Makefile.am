bin_PROGRAMS = omshell
lib_LIBRARIES = libdhcpctl.a
noinst_PROGRAMS = cltest
man_MANS = omshell.1 dhcpctl.3
EXTRA_DIST = $(man_MANS)

omshell_SOURCES = omshell.c
omshell_LDADD = libdhcpctl.a ../common/libdhcp.a ../omapip/libomapi.a \
	       $(EXPORT_DIR)/libdns.a $(EXPORT_DIR)/libisc.a \
	       -lgssapi_krb5 -lkrb5 -lgss -lcrypto

libdhcpctl_a_SOURCES = dhcpctl.c callback.c remote.c

cltest_SOURCES = cltest.c
cltest_LDADD = libdhcpctl.a ../common/libdhcp.a ../omapip/libomapi.a \
	       $(EXPORT_DIR)/libdns.a $(EXPORT_DIR)/libisc.a \
	       -lgssapi_krb5 -lkrb5 -lgss -lcrypto

