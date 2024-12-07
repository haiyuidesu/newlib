# Newlib

This repository contains a Newlib port for bare-metal AArch64 with custom system ABI (aarch64-elf).

It is based on the [checkra1n](https://checkra.in/) project's [newlib](https://github.com/checkra1n/newlib) but for my own purposes.

## Building

On macOS with Xcode installed, or on Linux with `clang`/`llvm-ar`/`llvm-ranlib` and `ld.lld` installed:

```makefile
make
```
If you need to adjust any of the paths or options:

```makefile
EMBEDDED_CC="path/to/clang" \
EMBEDDED_CFLAGS="<whatever>" \
EMBEDDED_LDFLAGS="-fuse-ld=path/to/ld.lld" \
EMBEDDED_AR="path/to/llvm-ar" \
EMBEDDED_RANLIB="path/to/llvm-ranlib" \
make
```

If there are further defaults you need to override, see `EMBEDDED_CC_FLAGS` and `EMBEDDED_LD_FLAGS` in the `Makefile`.
