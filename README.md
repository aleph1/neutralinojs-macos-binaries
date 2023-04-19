# Compiled Neutralinojs Binaries for macOS 11
Newer versions of [Neutralinojs](https://github.com/neutralinojs/neutralinojs) include binaries for macOS 12+ only. This repo includes compiled versions for macOS 11 that resolve crashes when trying to run the newer binaries see: https://github.com/neutralinojs/neutralinojs/issues/265.

**Note:** Using the binaries in this repo comes with the inherent risk of downloading compiled binaries, and any security issues present in neutralinojs will also be found in these compiled versions. These binaries were built as follows:

- cloned the neutralinojs repo (https://github.com/neutralinojs/neutralinojs)
- compiled for x64 (% python3 scripts/bz.py --verbose --target_arch=x64)
- compiled for arm64 (% python3 scripts/bz.py --verbose --target_arch=arm64)

For versions 4.10.0+, no changes have been made to the neutralinojs code.

For versions <=4.9.0 I had to copy the /lib/tray/tray.h file from a newer version of neutralinojs to get the code to compile, so I can’t guarantee the tray code will work as expected (I have not tested this).

If you need other versions compiled just create an issue.
