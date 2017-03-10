Gello Build System
==================

Inline build environment for Gello

Documentation
-------------

Features
----------
- *--clean* = Make a clean build
- *--depot* = Install Depot Tool
- *--fast* = Skip sync and runhooks, useful for testing changes
- *--no-sync* = Skip sync

How to build
----------
If you're going to build from LineageOS build environment you will be able to choose between Sourcebuilt or Prebuilt. By default LineageOS uses Prebuilt to save you time, data and disk space.
If you don't want to use/trust prebuilt apk (that comes from CyanogenMod Maven) for some reason, you're free to build it yourself on your own machine. To build from source you just need to run the following commands:

    export WITH_GELLO_SOURCE=true
    mka Gello
To be able to build Gello you'll need to set up your machine, see [Setup](https://github.com/LineageOS/android_external_gello_build#setup).

Testing
----------
If you're working on the Gello channel, you may want to use your local channel instead of Lineage one. 

    export WITH_GELLO_SOURCE=true
    croot
    cd external/gello-build/env/swe/channels
    rm -rf lineage
    git clone https://your.git.repo/my_cool_channel lineage 
    mka Gello

Setup
----------
Read [chromium documentation](https://chromium.googlesource.com/chromium/src/+/master/docs/linux_build_instructions_prerequisites.md) for needed packages to build Gello.
To get sources you need Depot tools that can be easily installed by running

    ./gello_build.sh --depot

During the first build you may be asked to accept EULA for some components needed to compile.
__Building from source is not recommend to those who have a really limited storage and / or data plan, the Gello environment needs to download a lot of data__
