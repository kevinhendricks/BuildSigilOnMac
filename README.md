Building Sigil on Mac OSX 
==========================

Sigil is a free, open source, multi-platform ebook editor that uses
Qt (and QtWebEngine). It is designed to edit books in ePub format (both ePub 2 and ePub 3).

To build Sigil master from source requires a complete build of Qt 5.12.6 
and Python 3.7.2.

This repository is used to keep prebuilt binaries for these main build
prerequisites to make building Sigil itself on macOS much easier.  And
to enable automation the Sigil build process on macOS via Travis CI.


For Building on Mac OS X
========================

Building using purely XCode is no longer supported on Mac OS X.  The easiest 
way to build Sigil on Mac OS X is to use cmake 3.0 and the command line.   

Also because Sigil now embeds Python 3.7.2, see  

> [Building_A_Relocatable_Python_3.7_Framework_on_MacOSX.txt](./Building_A_Relocatable_Python_3.7_Framework_on_MacOSX.txt)

for detailed instructions on how to build a fully relocatable Python 3.7.X framework before
building Sigil.  

Sigil uses Qt-5.12.6 currently, see  

> [Building_Qt5_From_Source_on_MacOSX.txt](./Building_Qt5_From_Source_on_MacOSX.txt)


And finally to build Sigil itself see:

> [Building_Sigil_On_MacOSX.txt](./Building_Sigil_On_MacOSX.txt)

Pre-built binaries packaged as zip archives are provided for the following
packages:


xz-5.2.4 (unpack and sudo make install to install into /usr/local)

Python-3.7.2 plus modifications to make the framework fully relocatable.

Qt5.12.6 with a number of backported patches and fixes to make Qt5.12.6 usable and 
configured to enable proprietary-codecs in QtWebEngine
