Building Sigil on Mac OSX 
==========================

Sigil is a free, open source, multi-platform ebook editor that uses
Qt (and QtWebEngine). It is designed to edit books in ePub format (both ePub 2 and ePub 3).

To build current Sigil master from source needs a complete build of Qt 6.5.2
and Python 3.11.3.

This repository is used to keep prebuilt binaries for these main build
prerequisites to make building Sigil itself on macOS much easier.  And
to enable automation the Sigil build process on macOS via Travis CI.


For Building on Mac OS X
========================

Building using purely XCode is no longer supported on Mac OS X.  The easiest 
way to build Sigil on Mac OS X is to use cmake 3.0 and the command line.   

Also because Sigil now embeds Python 3.11.3, see  

> [Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt](./Python/Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt)

for detailed instructions on how to build a fully relocatable Python 3.11 framework before
building Sigil.  

Sigil uses Qt-6.5.2 currently, see  

> [Building_Qt6_From_Source_on_MacOSX.txt](./Qt6.5/Building_Qt6_From_Source_on_MacOSX.txt)


And finally to build Sigil itself see:

> [Building_Sigil_On_MacOSX.txt](./Building_Sigil_On_MacOSX_With_Qt6.txt)

Pre-built binaries packaged as zip archives are provided for the following
packages:


xz-5.2.4 (unpack and sudo make install to install into /usr/local)

Python-3.11.3 plus modifications to make the framework fully relocatable.

Qt6.5.2 with a number of patches and bug fixes to make Qt6.5.2 usable and 
configured to enable proprietary-codecs in QtWebEngine
