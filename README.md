# AXEL

#### Axel — Light command line download accelerator for Linux and Unix

## 1. Help this project ##

Axel needs your help. **If you are a programmer** and if you wants to
help a nice project, this is your opportunity.

Axel was imported from its old repository[1] to GitHub (the original
homepage and developers are inactive). After this, all patches found
in Debian project and other places for this program were applied. All
initial work was registered in ChangeLog file (version 2.5 and later
releases). Axel is being packaged in Debian[2].

If you are interested to help Axel, read the [CONTRIBUTING.md](CONTRIBUTING.md) file.
Additionally, there is a group to discuss and to coordinate the
development process[3]. You can also find other developers in the
#axel channel on freenode.

[1] https://alioth.debian.org/projects/axel
[2] https://packages.qa.debian.org/a/axel.html
[3] https://groups.google.com/forum/#!forum/axel-accelerator-dev

## 2. What is Axel? ##

Axel tries to accelerate the downloading process by using multiple
connections for one file, similar to DownThemAll and other famous
programs. It can also use multiple mirrors for one download.

Using Axel, you will get files faster from Internet. So, Axel can
speed up a download up to 60% (approximately, according to some tests).

Axel tries to be as light as possible, so it might be useful as a
wget clone (and other console based programs) on byte-critical systems.

Axel supports HTTP, HTTPS, FTP and FTPS protocols.

Axel was originally developed by Wilmer van der Gaast. Thanks for your
efforts. Over time, Axel got several contributions from people. Please,
see AUTHORS and CREDITS files in source code.

## Building from source ##

Release tarballs contain a pre-generated buildsystem, but if you need to
edit/patch it, or you're building from a copy of the repository, then you may
need to run `autoreconf -i` to generate it. Further instructions are provided in
the [INSTALL](INSTALL) file. The basic actions for most users are:

    ./configure && make && make install

To build without SSL/TLS support, use `./configure --without-ssl`.

### Dependencies for release tarballs ###

* `gettext` (or `gettext-tiny`)
* `pkg-config`

Optional:

* `libssl` (OpenSSL, LibreSSL or compatible) -- for SSL/TLS support.

### Extra dependencies for building from snapshots ###

* `autoconf-archive`
* `autoconf`
* `automake`
* `autopoint`

### Building on Ubuntu from Git ###

#### Packages ####

* `build-essetial`
* `autoconf`
* `autoconf-archive`
* `automake`
* `autopoint`
* `gettext`
* `libssl-dev`
* `pkg-config`

### Build instrucitons ###

	$ autoreconf -fiv
	$ ./configure && make && sudo make install

## Mac OS X ##
### Install with Homebrew ###

    brew install axel

### Building ##

Install the following homebrew packages: `brew install automake gettext openssl`

You'll need to provide some extra options to `autogen.sh` and `configure`
so they can find gettext and openssl.

```shell
GETTEXT=/usr/local/opt/gettext
OPENSSL=/usr/local/opt/openssl
PATH="$GETTEXT/bin:$PATH"
./autogen.sh -I$GETTEXT/share/aclocal/
CFLAGS="-I$GETTEXT/include -I$OPENSSL/include" LDFLAGS=-L$GETTEXT/lib ./configure
```

You can just run `make` as usual after these steps.

## Related projects ##

* [aria2](https://github.com/aria2/aria2)
* [hget](https://github.com/huydx/hget)
* [lftp](https://github.com/lavv17/lftp)
* [nugget](https://github.com/maxogden/nugget)
* [pget](https://github.com/Code-Hex/pget)

## License ##

Axel is under GPL-2+ with OpenSSL exception.
