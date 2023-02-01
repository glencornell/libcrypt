ACLOCAL_AMFLAGS = -I m4

lib_LIBRARIES = libcrypt.a

if CRYPT_SHA256
SHA256_SOURCES = sha256.h sha256.c sha256-crypt.c
SHA256_CFLAGS = -D__UCLIBC_HAS_SHA256_CRYPT_IMPL__
endif

if CRYPT_SHA512
SHA512_SOURCES = sha512.h sha512.c sha512-crypt.c
SHA512_CFLAGS = -D__UCLIBC_HAS_SHA512_CRYPT_IMPL__
endif

libcrypt_a_SOURCES = \
	crypt.c \
	des.c \
	md5.c \
	libcrypt.h \
	$(SHA256_SOURCES) \
	$(SHA512_SOURCES)

include_HEADERS = crypt.h

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libcrypt.pc

EXTRA_DIST = $(pkgconfig_DATA)

DISTCLEANFILES = $(pkgconfig_DATA)
