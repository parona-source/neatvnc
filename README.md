# Neat VNC

## Introduction
This is a liberally licensed VNC server library that's intended to be fast and
neat.

## Goals
 * Speed.
 * Clean interface.
 * Interoperability with the Freedesktop.org ecosystem.

## Building
```
make 
```

### Installing
```
make install
```

### Variables
 * `CFLAGS`: Flags passed to the compiler.
 * `LDFLAGS`: Flags passed to the linker.
 * `BUILD_DIR`: Destination directory for the build.
 * `PREFIX`: System prefix. Default: `/usr/local`.
 * `PKGCONFIG`: `pkg-config` executable path.
 * `STRIP`: `strip` executable path.
 * `DONT_STRIP`: Set this is the installed DSO is not to be stripped of its
   debugging symbols.

### Cross-compiling
Generally, it should be enough to set `CC=<architecture-triplet>-gcc` and then
run `make`, e.g.:
```
CC=arm-linux-gnueabihf-gcc make
```
If you have a `pkg-config` wrapper at `<triplet>-pkg-config` it will be run
instead if `pkg-config`, but pkg-config can also be overridden by setting the
`PKGCONFIG` environment variable prior to running `make`.
