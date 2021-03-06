#-------------------------------------------------------------------------
#
# Makefile.am for psqlodbc30w (PostgreSQL ODBC driver)
#
#-------------------------------------------------------------------------

AUTOMAKE_OPTIONS = 1.8 foreign

ACLOCAL_AMFLAGS = -I config

if enable_unicode
lib_LTLIBRARIES = agodbcw.la
else
lib_LTLIBRARIES = agodbca.la
endif

AM_LDFLAGS = -module -no-undefined -avoid-version -export-symbols-regex '^SQL'

agodbca_la_SOURCES = \
	info.c bind.c columninfo.c connection.c convert.c drvconn.c \
	environ.c execute.c lobj.c misc.c options.c \
	pgtypes.c psqlodbc.c qresult.c results.c parse.c \
	statement.c tuple.c dlg_specific.c \
	multibyte.c odbcapi.c descriptor.c \
	odbcapi30.c pgapi30.c mylog.c \
\
	bind.h catfunc.h columninfo.h connection.h convert.h \
	descriptor.h dlg_specific.h environ.h \
	lobj.h misc.h multibyte.h pgapifunc.h pgtypes.h \
	psqlodbc.h qresult.h resource.h statement.h tuple.h \
	version.h pgenlist.h mylog.h xalibname.h

agodbcw_la_SOURCES = $(agodbca_la_SOURCES) \
	odbcapi30w.c odbcapiw.c win_unicode.c


EXTRA_DIST = license.txt readme.txt readme_winbuild.txt \
	psqlodbc.def psqlodbca.def editConfiguration.bat BuildAll.bat \
	windows-defaults.mak \
	pgenlist.def pgenlista.def connexp.h \
	dlg_wingui.c loadlib.c loadlib.h inouealc.c win_setup.h \
        setup.c win_unicode.c psqlodbc.rc win64.mak \
        psqlodbc.reg psqlodbc.dsp psqlodbc.vcproj \
        psqlodbc.sln msdtc_enlist.cpp pgxalib.cpp xalibname.c \
        pgxalib.def odbc.sql odbc-drop.sql \
\
	docs/config-opt.html \
	docs/config.html \
	docs/README.txt \
	docs/release-7.3.html \
	docs/release.html \
	docs/unix-compilation.html \
	docs/win32-compilation.html \
	docs/msdtc_pgxalib_tracing_enable.reg \
	docs/msdtc_pgxalib_tracing_disable.reg \
	docs/msdtc_pgxalib_tracing_README.txt \
\
	installer/background.bmp \
	installer/banner.bmp \
	installer/buildInstallers.ps1 \
	installer/installer.mak \
	installer/lgpl.rtf \
	installer/modify_msi.vbs \
	installer/productcodes.mak \
	installer/psqlodbc-setup \
	installer/README.txt \
	installer/upgrade.bat \
	installer/upgrade_x64.bat \
	installer/psqlodbcm_cpu.wxs \
	installer/psqlodbc_cpu.wxs \
	installer/psqlodbc-setup/buildBootstrapper.ps1 \
	installer/psqlodbc-setup/Bundle.wxs \
	installer/psqlodbc-setup/Make.bat \
	installer/psqlodbc-setup/psqlodbc-setup.wixproj \
	installer/psqlodbc-setup/vcredist.wxs \
\
	winbuild/BuildAll.ps1 \
	winbuild/configuration.ps1 \
	winbuild/configuration_template.xml \
	winbuild/editConfiguration.ps1 \
	winbuild/pgenlist.vcxproj \
	winbuild/pguser.Cpp.props \
	winbuild/pgxalib.vcxproj \
	winbuild/platformbuild.vcxproj \
	winbuild/psqlodbc.Cpp.props \
	winbuild/psqlodbc.vcxproj \
	winbuild/readme.txt \
\
	test/Makefile.in \
	test/odbcini-gen.sh \
	test/README.txt \
	test/reset-db.c \
	test/runsuite.c \
	test/sampletables.sql \
	test/tests \
	test/win.mak \
	test/Makefile \
	test/expected \
	test/src 

MAINTAINERCLEANFILES = \
	Makefile.in config/config.guess config.h.in config/config.sub configure \
	config/install-sh config/missing aclocal.m4 config/ltmain.sh \
	config/depcomp
