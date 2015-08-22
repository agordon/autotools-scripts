# Autotools for Scripts - Template Project

This template project demostrate how to use GNU autotools (autoconf+
automake) to package a shell script (with optional data files).

## Usage

The autotools build systems enables the following:

    # required if checked out from git
    ./bootstrap

    # generate the scripts ('input' from 'input.sh'),
    # with the custom PATH and option (foobar)
    ./configure --prefix /tmp/demo --enable-foobar

    # install the script in /tmp/demo/bin/input ,
    # and the data file in /tmp/demo/share/autotools-scripts/examples/ .
    make install

## Prepare a new official release version

    # After all changes are commited, tag a new version.
    # tag must start with 'v' (for 'config/git-version-gen').
    git tag -a 'v0.0.3' -m 'version v0.0.3'

    # rebuild
    ./bootstrap && ./configure

    # Create tarball file
    make dist

This will generate a new tar.gz file with the correct version
(e.g. `autotools-scripts-0.0.3.tar.gz`). This file should be made public,
then users can run:

    wget http://my.server.com/downloads/autotools-scripts-0.0.3.tar.gz
    tar -xzf autotools-scripts-0.0.3.tar.gz
    cd autotools-scripts-0.0.3
    ./configure
    make install

Which will install the script to `/usr/local/bin` and the data file to
`/usr/local/share/autotools-scripts/examples` (unless `--prefix` is used).

## More information

contact: Assaf Gordon (assafgordon@gmail.com)
License: MIT (support script `git-version-gen` is GPLv3+)
Website: https://github.com/agordon/autotools-scripts
