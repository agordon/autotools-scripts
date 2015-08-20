
EXTRA_DIST = $(top_srcdir)/.version

BUILT_SOURCES = $(top_srcdir)/.version

# Scripts which will be installed in
# /usr/local/bin (or other location with --prefix)
bin_SCRIPTS = \
	input

# files to install in /usr/local/share/PACKAGE/examples
examplesdir = $(pkgdatadir)/examples
dist_examples_DATA = data.txt
EXTRA_DIST += $(dist_examples_DATA)


# Makefile commands to generate version file for tarball distribution.
$(top_srcdir)/.version:
	            echo $(VERSION) > $@-t && mv $@-t $@

dist-hook:
	            echo $(VERSION) > $(distdir)/.tarball-version
