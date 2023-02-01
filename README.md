# libcrypt

Crypt library for DES, MD5 for uClibc

## Description

The primary purpose of this library was to port it to the ESP32 MCU as
a dependency for libpcap.

This code has been extracted from [uclibc-ng](https://cgit.uclibc-ng.org/cgi/cgit/uclibc-ng.git/tree/libcrypt).

## Build

```bash
autoreconf -vi
./configure
make
```

## Copyright

Copyright (C) 2000-2006 by Erik Andersen <andersen@uclibc.org>

## License

Licensed under the LGPL v2.1, see the file COPYING.LIB in this tarball.

