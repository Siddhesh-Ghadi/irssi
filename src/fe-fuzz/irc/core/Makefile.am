bin_PROGRAMS = event-get-params-fuzz

# Force link with CXX for libfuzzer support
CCLD=$(CXX) $(CXXFLAGS)

AM_CPPFLAGS = \
	$(GLIB_CFLAGS)

LDADD = \
	../../../irc/libirc.a \
	../../../irc/core/libirc_core.a \
	../../../irc/dcc/libirc_dcc.a \
	../../../irc/flood/libirc_flood.a \
	../../../irc/notifylist/libirc_notifylist.a \
	../../../fe-common/core/libfe_common_core.a \
	../../../fe-common/irc/libfe_common_irc.a \
	../../../fe-common/irc/dcc/libfe_irc_dcc.a \
	../../../fe-common/irc/notifylist/libfe_irc_notifylist.a \
	../../../core/libcore.a \
	../../../lib-config/libirssi_config.a \
	@PROG_LIBS@ \
	$(FUZZER_LIBS)

event_get_params_fuzz_SOURCES = \
        ../../null-logger.c \
        event-get-params.c \
	$(top_srcdir)/src/fe-text/module-formats.c

noinst_HEADERS = \
	$(top_srcdir)/src/fe-text/module-formats.h
