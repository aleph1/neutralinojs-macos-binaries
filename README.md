# Compiled macOS Binaries for Neutralinojs
Newer versions of [Neutralinojs](https://github.com/neutralinojs/neutralinojs) include binaries for macOS 12+. This repo includes compiled versions for macOS 11 that resolve crashes when trying to run the newer binaries see: https://github.com/neutralinojs/neutralinojs/issues/265.

These binaries were built as follows:

- cloned the neutralinojs repo (https://github.com/neutralinojs/neutralinojs)
- compiled for x64 (% python3 scripts/bz.py --verbose --target_arch=x64)
- compiled for arm64 (% python3 scripts/bz.py --verbose --target_arch=arm64)

No changes have been made to the neutralinojs code, but using them for a release application comes with the inherent risks of downloading compiled binaries, and any security issues present in neutralinojs will also be found in these compiled versions.

Vesions <4.10.0 have an issue with tray.h compiling for macOS 11. It might be possible to get these compiling, but I would likely have to backport changes for tray.h. If possible, upgrade to v4.10.0 or greater.
