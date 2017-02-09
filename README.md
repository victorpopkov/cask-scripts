# cask-scripts

[![Build Status](https://travis-ci.org/victorpopkov/cask-scripts.svg?branch=master)](https://travis-ci.org/victorpopkov/cask-scripts)

Collection of small scripts designed to help maintain the [Homebrew-Cask](https://github.com/caskroom/homebrew-cask)
project. The main purpose, however, is to completely automate the process of
finding and upgrading outdated casks.

- [List of scripts](#description)
  - [cask-appcast](#cask-appcast)
  - [cask-check-updates](#cask-check-updates)
  - [cask-homepage](#cask-homepage)
- [Installation](#installation)
  - [Linux](#linux)
  - [macOS](#macos)
- [Running tests](#running-tests)

## List of scripts

To learn more about each script explore [doc](doc/) directory.

### [cask-appcast](doc/cask-appcast.md)

Get the latest available version, checkpoint and download URL(s) from appcast.
[Learn more...](doc/cask-appcast.md)

<img src="http://caskroom.victorpopkov.com/cask-scripts/cask-appcast.gif" data-canonical-src="http://caskroom.victorpopkov.com/cask-scripts/cask-appcast.gif" width="400" />

### [cask-check-updates](doc/cask-check-updates.md)

Scan casks with appcasts for outdated ones and get the latest available
version(s).
[Learn more...](doc/cask-check-updates.md)

<img src="http://caskroom.victorpopkov.com/cask-scripts/cask-check-updates.gif" data-canonical-src="http://caskroom.victorpopkov.com/cask-scripts/cask-check-updates.gif" width="400" />

### [cask-homepage](doc/cask-homepage.md)

Check homepages of the casks and try to fix them. [Learn more...](doc/cask-homepage.md)

Suggested by [**@miccal**](https://github.com/miccal).

<img src="http://caskroom.victorpopkov.com/cask-scripts/cask-homepage.gif" data-canonical-src="http://caskroom.victorpopkov.com/cask-scripts/cask-homepage.gif" width="400" />

## Installation

### Linux

Even though [Homebrew-Cask](https://github.com/caskroom/homebrew-cask) was
created specifically for macOS, most of the scripts provided in the current
repository can be used on Linux. The installation procedure is quite simple:
just clone this repository somewhere on your system and then use `install`
target of the provided Makefile:

```bash
git clone https://github.com/victorpopkov/cask-scripts.git
cd cask-scripts
make install
```

The same thing goes for uninstallation procedure: just use `uninstall` target if
you would like to completely remove `cask-scripts` from your system.

#### Dependencies

The scripts need [jq](https://github.com/stedolan/jq) and
[xmlstarlet](http://xmlstar.sourceforge.net/) to be installed on your system.
To install both on Linux just run:

```bash
apt-get install jq xmlstarlet
```

### macOS

The easiest way to install these scripts on macOS is using my
[homebrew-tap](https://github.com/victorpopkov/homebrew-tap)
repository. You’ll need [Homebrew](http://brew.sh/) installed and then:

```bash
brew install victorpopkov/tap/cask-scripts
```

Alternatively, you can use install target of the provided Makefile the same way
as you would install them on Linux. However, using [Homebrew](http://brew.sh/)
is the more recommended way for macOS, since it also installs all the
dependencies.

## Running tests

For testing purposes, [Bats](https://github.com/sstephenson/bats) is bundled
into this project. In order to run the tests simply use `test` target of the
provided Makefile: `make test`

## License

Released under the [MIT License](https://opensource.org/licenses/MIT).
