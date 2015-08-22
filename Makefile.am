# autotools-scripts: Template project of autotools for scripts
# copyright (C) Assaf Gordon <assafgordon@gmail.com>
# License: MIT
# See: https://github.com/autotools-scripts

EXTRA_DIST = $(top_srcdir)/.version

BUILT_SOURCES = $(top_srcdir)/.version

# Scripts which will be installed in
# /usr/local/bin (or other location with --prefix)
#
# NOTE: this script is generated from 'autotools-script-demo.sh.sh'
#       by running ./configure.
bin_SCRIPTS = \
	autotools-script-demo

# files to install in /usr/local/share/PACKAGE/examples
examplesdir = $(pkgdatadir)/examples
dist_examples_DATA = data.txt
EXTRA_DIST += $(dist_examples_DATA)


# Makefile commands to generate version file for tarball distribution.
$(top_srcdir)/.version:
	            echo $(VERSION) > $@-t && mv $@-t $@

dist-hook:
	            echo $(VERSION) > $(distdir)/.tarball-version
