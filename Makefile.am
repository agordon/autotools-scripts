
EXTRA_DIST = $(top_srcdir)/.version

BUILT_SOURCES = $(top_srcdir)/.version

bin_SCRIPTS = \
	input

$(top_srcdir)/.version:
	            echo $(VERSION) > $@-t && mv $@-t $@

dist-hook:
	            echo $(VERSION) > $(distdir)/.tarball-version
