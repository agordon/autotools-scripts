AC_INIT([dnaland2-scripts],
        m4_esyscmd([config/git-version-gen .tarball-version]),
	[assafgordon@gmail.com])

AC_CONFIG_AUX_DIR(config)
AM_INIT_AUTOMAKE([foreign])
AC_CONFIG_MACRO_DIR([m4])

AC_PROG_LN_S

AC_SUBST(VERSION)

AC_CONFIG_FILES( [
		  Makefile
          input:input.sh
          other:other.sh
		  ] )

AC_OUTPUT()
