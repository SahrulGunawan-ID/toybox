# Build Toybox 0.8.9 2025

---

# Building Toybox 0.8.9 (AArch64)

This guide documents the build process and output for compiling **Toybox 0.8.9** on an AArch64 environment. The steps cover cleaning, configuration, building, and verifying the resulting binary.

---

## 🧹 Clean Environment

```bash
make clean
make distclean
```

Output:
```
cleaned
chmod: generated: No such file or directory
cleaned
root cleaned
removed .config
```

---

## ⚙️ Configuration

```bash
./configure
```

Output:
```
Assuming you want 'make defconfig'...
cc -o kconfig/conf ...
scripts/genconfig.sh
kconfig/conf -D /dev/null Config.in > /dev/null
```

---

## 📁 Directory Structure After Configuration

```
Config.in  LICENSE    Makefile   README     build.rc
configure  generated  kconfig    lib        main.c
scripts    tests      toybox     toys       toys.h
www
```

---

## 🏗️ Build Process

```bash
bash run_build.rc
```

Output:
```
cleaned
scripts/genconfig.sh
scripts/make.sh
Library probe
generated/{...}
Compile toybox
..................................................................
```

---

## ✅ Verification

Run the compiled Toybox:

```bash
./toybox
```

Expected output: List of supported commands (e.g., `ls`, `cp`, `mount`, `reboot`, etc.)

Check binary type:

```bash
file toybox
```

Output:
```
toybox: ELF 64-bit LSB executable, ARM aarch64, statically linked, stripped
```

---

## ℹ️ Usage Help

```bash
./toybox --help
```

Toybox supports both single-call and multi-call usage patterns. For more usage tips, see [Toybox FAQ](https://landley.net/toybox/faq.html#install).

---
# OS DOWNLOAD :
https://alpinelinux.org/downloads/

# ADDONS COMPILE TOYBOX OR MORE
```` bash
apk add 7zip
apk add acl-libs
apk add ada-libs
apk add alpine-baselayout
apk add alpine-baselayout-data
apk add alpine-keys
apk add alpine-release
apk add apache2
apk add apk-tools
apk add apr
apk add apr-util
apk add argon2-libs
apk add autoconf
apk add automake
apk add bash
apk add bc
apk add binutils
apk add binutils-dev
apk add bison
apk add brotli-libs
apk add bsd-compat-headers
apk add build-base
apk add busybox
apk add busybox-binsh
apk add bzip2-dev
apk add c-ares
apk add ca-certificates
apk add ca-certificates-bundle
apk add check
apk add clang20
apk add clang20-headers
apk add clang20-libs
apk add cmake
apk add cpio
apk add curl
apk add diffutils
apk add dosfstools
apk add dtc
apk add e2fsprogs
apk add e2fsprogs-libs
apk add elfutils-dev
apk add file
apk add flex
apk add fortify-headers
apk add g++
apk add gawk
apk add gcc
apk add gcc-gdb
apk add gcompat
apk add gcovr
apk add gcovr-pyc
apk add gdb
apk add gdbm
apk add gettext
apk add gettext-asprintf
apk add gettext-dev
apk add gettext-envsubst
apk add gettext-libs
apk add git
apk add git-init-template
apk add git-perl
apk add glib
apk add gmp
apk add grep
apk add icu-data-en
apk add icu-libs
apk add isl26
apk add jansson
apk add jq
apk add lcov
apk add libapk2
apk add libarchive
apk add libasm
apk add libatomic
apk add libblkid
apk add libburn
apk add libbz2
apk add libcap-dev
apk add libcap-static
apk add libcap2
apk add libcom_err
apk add libcrypto3
apk add libcurl
apk add libdw
apk add libeconf
apk add libedit
apk add libedit-dev
apk add libelf
apk add libevent
apk add libevent-dev
apk add libexpat
apk add libfdt
apk add libffi
apk add libffi-dev
apk add libformw
apk add libgcc
apk add libgomp
apk add libhistory
apk add libidn2
apk add libidn2-dev
apk add libidn2-static
apk add libintl
apk add libisoburn
apk add libisofs
apk add libltdl
apk add libmagic
apk add libmenuw
apk add libmount
apk add libncurses++
apk add libncursesw
apk add libpanelw
apk add libpcre2-16
apk add libpcre2-32
apk add libpsl
apk add libpsl-dev
apk add libpsl-static
apk add libpsl-utils
apk add libselinux
apk add libselinux-dev
apk add libsepol
apk add libsepol-dev
apk add libssh2
apk add libssh2-dev
apk add libssh2-static
apk add libssl3
apk add libstdc++
apk add libstdc++-dev
apk add libtool
apk add libucontext
apk add libucontext-dev
apk add libunistring
apk add libunistring-dev
apk add libunistring-static
apk add libunwind
apk add libunwind-dev
apk add libuuid
apk add libuv
apk add libuv-dev
apk add libxml2
apk add libxslt
apk add libxxhash
apk add linux-headers
apk add lld20
apk add lld20-libs
apk add llvm20-libs
apk add llvm20-linker-tools
apk add ltrace
apk add lz4-dev
apk add lz4-libs
apk add lzo
apk add m4
apk add make
apk add mpc1
apk add mpdecimal
apk add mpfr4
apk add musl
apk add musl-dbg
apk add musl-dev
apk add musl-fts
apk add musl-obstack
apk add musl-utils
apk add nano
apk add ncurses
apk add ncurses-dev
apk add ncurses-static
apk add ncurses-terminfo-base
apk add nghttp2-dev
apk add nghttp2-libs
apk add nghttp2-static
apk add nodejs
apk add npm
apk add oniguruma
apk add openssl-dev
apk add openssl-libs-static
apk add patch
apk add pcre2
apk add pcre2-dev
apk add pcre2-static
apk add perl
apk add perl-b-hooks-endofscope
apk add perl-capture-tiny
apk add perl-class-data-inheritable
apk add perl-class-inspector
apk add perl-class-singleton
apk add perl-clone
apk add perl-common-sense
apk add perl-datetime
apk add perl-datetime-locale
apk add perl-datetime-timezone
apk add perl-devel-stacktrace
apk add perl-digest-md5
apk add perl-dist-checkconflicts
apk add perl-error
apk add perl-eval-closure
apk add perl-exception-class
apk add perl-file-sharedir
apk add perl-git
apk add perl-json-xs
apk add perl-memory-process
apk add perl-memory-usage
apk add perl-module-implementation
apk add perl-module-runtime
apk add perl-mro-compat
apk add perl-namespace-autoclean
apk add perl-namespace-clean
apk add perl-package-stash
apk add perl-params-validationcompiler
apk add perl-readonly
apk add perl-role-tiny
apk add perl-specio
apk add perl-sub-exporter-progressive
apk add perl-sub-quote
apk add perl-test-fatal
apk add perl-test-simple
apk add perl-test-without-module
apk add perl-test2-plugin-nowarnings
apk add perl-time-hires
apk add perl-timedate
apk add perl-try-tiny
apk add perl-types-serialiser
apk add php83
apk add php83-common
apk add pkgconf
apk add popt
apk add py3-colorlog
apk add py3-colorlog-pyc
apk add py3-jinja2
apk add py3-jinja2-pyc
apk add py3-lxml
apk add py3-lxml-pyc
apk add py3-markupsafe
apk add py3-markupsafe-pyc
apk add py3-packaging
apk add py3-packaging-pyc
apk add py3-parsing
apk add py3-parsing-pyc
apk add py3-pip
apk add py3-pip-pyc
apk add py3-pygments
apk add py3-pygments-pyc
apk add py3-setuptools
apk add py3-setuptools-pyc
apk add py3-talloc
apk add pyc
apk add python3
apk add python3-pyc
apk add python3-pycache-pyc0
apk add re2c
apk add readline
apk add readline-dev
apk add rhash-libs
apk add rsync
apk add samurai
apk add scanelf
apk add scudo-malloc
apk add simdjson
apk add simdutf
apk add sqlite-libs
apk add squashfs-tools
apk add ssl_client
apk add strace
apk add sudo
apk add talloc
apk add talloc-dev
apk add talloc-static
apk add tar
apk add tree
apk add tzdata
apk add unzip
apk add valgrind
apk add wget
apk add xorriso
apk add xz
apk add xz-dev
apk add xz-libs
apk add zip
apk add zlib
apk add zlib-dev
apk add zlib-static
apk add zstd
apk add zstd-dev
apk add zstd-libs
````
