<p align=center>
  <a href="http://98mebius.starfree.jp/reactos_jpn/">
    <img alt="ReactOS" src="http://98mebius.starfree.jp/reactos_jpn/images/reactos.png">
  </a>
</p>

---


## ReactOS 日本語版について

ReactOS™は、オープンソースで開発されている、Microsoft®Windows™NT互換のOSです。
Windows用に作成されたアプリケーションおよびドライバーとの互換性の実現を目指しています。
（ここでのWindows™NTとは、NT4, 2000, XP, Vista, 7, 8, 10などのNTファミリーを指します。）

そして、ReactOS 日本語版は、mebius(@98mebius)が独自にビルドした派生版です。
オリジナルのReactOS チームに公式に認められたバージョンではないことを予めご理解ください。

日本語版の詳細についてはhttp://98mebius.starfree.jp/reactos_jpn/をご覧ください。
本家の詳細については、https：//www.reactos.orgをご覧ください。


ReactOSのコードは [GNU GPL 2.0](https://github.com/reactos/reactos/blob/master/COPYING)のライセンスに準拠します。

***ReactOSは現在アルファ版の段階にあり、動作が不安定です。***

## Building

[![appveyor.badge]][appveyor.link] [![travis.badge]][travis.link] [![rosbewin.badge]][rosbewin.link] [![rosbeunix.badge]][rosbeunix.link] [![coverity.badge]][coverity.link]

To build the system it is strongly advised to use the _ReactOS Build Environment (RosBE)._
Up-to-date versions for Windows and for Unix/GNU-Linux are available from our download page at: ["Build Environment"](http://www.reactos.org/wiki/Build_Environment).

Alternatively one can use Microsoft Visual C++ (MSVC) version 2010+. Building with MSVC is covered here: ["Visual Studio or Microsoft Visual C++"](https://www.reactos.org/wiki/CMake#Visual_Studio_or_Microsoft_Visual_C.2B.2B).

### Binaries

To build ReactOS you must run the `configure` script in the directory you want to have your build files. Choose `configure.cmd` or `configure.sh` depending on your system. Then run `ninja <modulename>` to build a module you want or just `ninja` to build all modules.

### Bootable images

To build a bootable CD image run `ninja bootcd` from the
build directory. This will create a CD image with a filename `bootcd.iso`.

See ["Building ReactOS"](http://www.reactos.org/wiki/Building_ReactOS) for more details.

You can always download fresh binary builds of bootable images from the ["Daily builds"](https://www.reactos.org/getbuilds/) page.

## Installing

By default, ReactOS currently can only be installed on a machine that has a FAT16 or FAT32 partition as the active (bootable) partition. 
The partition on which ReactOS is to be installed (which may or may not be the bootable partition) must also be formatted as FAT16 or FAT32.
ReactOS Setup can format the partitions if needed.

Starting 0.4.10, ReactOS can be installed using the BtrFS file system. But
consider this as an experimental feature and thus regressions not triggered on
FAT setup may be observed.

To install ReactOS from the bootable CD distribution, extract the archive contents. Then burn the CD image, boot from it, and follow the instructions.

See ["Installing ReactOS"](https://www.reactos.org/wiki/Installing_ReactOS) Wiki page or [INSTALL](INSTALL) for more details.

## Testing

If you discover a bug in ReactOS search on JIRA first - it might be reported already. If not report the bug providing logs and as much information as possible.

See ["File Bugs"](https://www.reactos.org/wiki/File_Bugs) for a guide.

__NOTE:__ The bug tracker is _not_ for discussions. Please use `#reactos` Freenode IRC channel or our [forum](https://reactos.org/forum).

## Contributing  ![prwelcome.badge]

We are always looking for developers! Check [how to contribute](CONTRIBUTING.md) if you are willing to participate.

You can also support ReactOS by [donating](https://reactos.org/donating)! We rely on our backers to maintain our servers and accelerate development by [hiring full-time devs](https://reactos.org/node/785).

## More information

ReactOS is a Free and Open Source operating system based on the Windows architecture, 
providing support for existing applications and drivers, and an alternative to the current dominant consumer operating system.

It is not another wrapper built on Linux, like WINE. It does not attempt or plan to compete with WINE; in fact, the user-mode part of ReactOS is almost entirely WINE-based and our two teams have cooperated closely in the past. 

ReactOS is also not "yet another OS". It does not attempt to be a third player like any other alternative OS out there. People are not meant to uninstall Linux and use ReactOS instead; ReactOS is a replacement for Windows users who want a Windows replacement that behaves just like Windows.

More information is available at: [reactos.org](https://www.reactos.org).

Also see the [media/doc](/media/doc/) subdirectory for some sparse notes.

## Who is responsible

Active devs are listed as members of [GitHub organization](https://github.com/orgs/reactos/people).
See also the [CREDITS](CREDITS) file for others.

## Code mirrors

The main development is done on [GitHub](https://github.com/reactos/reactos). We have an [alternative mirror](https://git.reactos.org/?p=reactos.git) in case GitHub is down.

There is also an obsolete [SVN archive repository](https://svn.reactos.org/reactos/) that is kept for historical purposes.

[travis.badge]:     https://travis-ci.org/reactos/reactos.svg?branch=master
[appveyor.badge]:   https://ci.appveyor.com/api/projects/status/github/reactos/reactos?branch=master&svg=true
[coverity.badge]:   https://scan.coverity.com/projects/205/badge.svg?flat=1
[rosbewin.badge]:   https://img.shields.io/badge/RosBE_Windows-2.1.6-0688CB.svg
[rosbeunix.badge]:  https://img.shields.io/badge/RosBE_Unix-2.1.2-0688CB.svg
[prwelcome.badge]:  https://img.shields.io/badge/PR-welcome-0688CB.svg

[travis.link]:      https://travis-ci.org/reactos/reactos
[appveyor.link]:    https://ci.appveyor.com/project/AmineKhaldi/reactos
[coverity.link]:    https://scan.coverity.com/projects/205
[rosbewin.link]:    https://sourceforge.net/projects/reactos/files/RosBE-Windows/i386/2.1.6/
[rosbeunix.link]:   https://sourceforge.net/projects/reactos/files/RosBE-Unix/2.1.2/
