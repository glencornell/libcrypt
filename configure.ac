#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.71])
AC_INIT([libcrypt],[0.0.1],[])

# Store the auxiliary build tools (e.g., install-sh, config.sub, config.guess)
# in this dir (build-aux)
AC_CONFIG_AUX_DIR([build-aux])

# Install m4 macros here
AC_CONFIG_MACRO_DIRS([m4])

AC_CONFIG_SRCDIR([sha256.c])
AC_CONFIG_HEADERS([config.h])

# Init automake, and specify this program use relaxed structures.
# i.e. this program doesn't follow the gnu coding standards, and
# doesn't have ChangeLog, COPYING, AUTHORS, INSTALL, README
# etc. files.
AM_INIT_AUTOMAKE([-Wall -Werror foreign])

# Checks for programs.
PKG_PROG_PKG_CONFIG
AM_PROG_AR
AC_PROG_CC
AC_PROG_RANLIB

# Checks for libraries.

# Checks for header files.
AC_CHECK_HEADERS([netinet/in.h stdint.h sys/param.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_TYPE_SIZE_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T

# Checks for library functions.
AC_FUNC_ALLOCA
AC_FUNC_REALLOC
AC_CHECK_FUNCS([mempcpy memset strcspn strtoul])

# Checks for user options
AC_ARG_ENABLE([sha256],
    AS_HELP_STRING([--disable-sha256], [Disable SHA256 hash]))
AM_CONDITIONAL([CRYPT_SHA256], [test "x$enable_sha256" != "xno"])

AC_ARG_ENABLE([sha512],
    AS_HELP_STRING([--disable-sha512], [Disable SHA512 hash]))
AM_CONDITIONAL([CRYPT_SHA512], [test "x$enable_sha512" != "xno"])


AC_CONFIG_FILES([Makefile libcrypt.pc])
AC_OUTPUT
