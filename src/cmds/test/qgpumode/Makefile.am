PROG_ROOT = ../..

AM_CFLAGS = -g -DTEST_FUNCTION -I${PROG_ROOT}/ -I${PROG_ROOT}/${PBS_MACH} --coverage

lib_LTLIBRARIES = libqgpumode.la

AM_LDFLAGS = @CHECK_LIBS@ ${lib_LTLIBRARIES}

check_PROGRAMS = test_qgpumode

libqgpumode_la_SOURCES = scaffolding.c ${PROG_ROOT}/qgpumode.c
libqgpumode_la_LDFLAGS = @CHECK_LIBS@ -shared -lgcov

test_qgpumode_SOURCES = test_qgpumode.c

check_SCRIPTS = ${PROG_ROOT}/../test/coverage_run.sh

TESTS = $(check_PROGRAMS) ${check_SCRIPTS}

CLEANFILES = *.gcno *.gcda *.gcov core *.lo
