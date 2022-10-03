# VlcMedia

Unreal Engine 5 Media Framework plug-in using the Video LAN Codec (libvlc v4).


## About

This plug-in is still under development and likely has a lot of remaining issues
to be fixed. Use in production is not yet recommended.

## Supported Platforms

This plug-in was last built against **Unreal Engine 5.0.3** and tested
against the following platforms:

- ~~Linux (Ubuntu 16.04)~~
- ~~Mac~~
- Windows

**IMPORTANT**: Please note that this repository contains pre-compiled binaries
for libvlc and its plug-ins, which are licensed under LGPL. This means that you
cannot create monolithic builds of your game without violating LGPL, the UE5
EULA or both. The libvlc libraries must remain dynamic libraries that are bound
at run-time - static linking is not allowed - and the licensing related files in
*/ThirdParty/vlc* must be retained.

This also means that this plug-in cannot work on platforms that do not support
dynamically linked libraries (i.e. iOS, HTML5) or do not currently implement
support for it (i.e. Android, XboxOne).

Epic is in the process of adding plug-in support to monolithic builds, but there
is no ETA yet. Once this is supported, you will be able to distribute monolithic
game and server builds with VlcMedia, provided that the libvlc libraries and
plug-ins remain as separate DLLs.


## Prerequisites

A relatively recent version of libvlc is required. The latest stable release
(currently 2.2.1) is not sufficient. However, newest nightly builds showed unstable
performance in context of UE Media Framework. Plugin update to latest libvlc WIP
(Fall 2022)

For Windows, the following nightly builds are currently included:
* Win64: vlc-4.0.0-dev-win64-249a76b9 (Spring 2022)


Nightly builds can be downloaded from the VideoLAN web site (see below).

For debug Win64, you should download debug builds and replace the
corresponding files and folders in the *VlcMedia/ThirdParty/vlc/* directory.

### Windows

All required libraries and plug-ins are included in the *ThirdParty* directory
and work out of the box.

## Dependencies

This plug-in requires Visual Studio and either a C++ code project or the full
Unreal Engine 4 source code from GitHub. If you are new to programming in UE4,
please see the official [Programming Guide](https://docs.unrealengine.com/latest/INT/Programming/index.html)! 

## Usage

You can use this plug-in as a project plug-in, or an Engine plug-in.

If you use it as a project plug-in, clone this repository into your project's
*/Plugins* directory and compile your game in Visual Studio. A C++ code project
is required for this to work.

If you use it as an Engine plug-in, clone this repository into the
*/Engine/Plugins/Media* directory and compile your game. Full Unreal Engine 4
source code from GitHub is required for this.


## References

* [VideoLAN Homepage](http://videolan.org)
* [VideoLAN Nightly Builds](http://nightlies.videolan.org/)
* [Introduction to UE4 Plugins](https://wiki.unrealengine.com/An_Introduction_to_UE4_Plugins)
