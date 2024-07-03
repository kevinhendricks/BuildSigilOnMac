Building Sigil on Mac OSX 
==========================

Sigil is a free, open source, multi-platform ebook editor that uses
Qt (and QtWebEngine). It is designed to edit books in ePub format (both ePub 2 and ePub 3).

To build current Sigil master from source uses a complete build of Qt 6.7.2
and Python 3.11.9 or later.

This repository is used to keep prebuilt binaries for these main build
prerequisites to make building Sigil itself on macOS much easier.  And
to enable automation the Sigil build process on macOS via Github Actions CI.


For Building on Mac OS X
========================

Building using purely XCode is no longer supported on Mac OS X.  The easiest 
way to build Sigil on Mac OS X is to use cmake 3.18 or later and the command line.   

Also because Sigil now embeds Python 3.11.9, see  

> [Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt](./Python/Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt)

for detailed instructions on how to build a fully relocatable Python 3.11 framework before
building Sigil.

Sigil uses Qt-6.7.2 currently, see  

> [Building_Qt6_From_Source_on_MacOSX.txt](./Qt6/Building_Qt6_From_Source_on_MacOSX.txt)


And finally to build Sigil itself see:

> [Building_Sigil_On_MacOSX.txt](./Building_Sigil_On_MacOSX_With_Qt6.txt)

Pre-built binaries packaged as zip archives are provided for the following
packages:


xz-5.2.4 (unpack and sudo make install to install into /usr/local)

Python-3.11.9 plus modifications to make the framework fully relocatable.

Qt6.7.2 needs a number of patches and bug fixes to make is usable and 
configured to enable proprietary-codecs in QtWebEngine.

