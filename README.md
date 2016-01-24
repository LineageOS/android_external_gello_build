Gello Build System
==================

Inline build environment for Gello

Documentation
-------------

Features
----------
- *--clean*     = Make a clean build
- *--depot*     = Install Depot Tool
- *--fast*      = Skip sync and runhooks, useful for testing changes
- *--local*     = Pick local gello from packages/apps/Gello (for testing purpose)
- *--push*      = Once everything else is done, install the given apk on a connected device
- *--no-sync*   = Skip sync

Setup
----------
Read [chromium documentation](https://chromium.googlesource.com/chromium/src/+/master/docs/linux_build_instructions_prerequisites.md) for needed packages to build Gello.
To get sources you need Depot tools that can be easily installed using _gello_build.sh --depot_
During the first build you may be asked to accept EULA for some components needed to compile.
