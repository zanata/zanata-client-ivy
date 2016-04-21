Zanata Java client script
-------------------------

Java command-line client for Zanata.

This repository doesn't include the actual Java code, just a shell script which uses
Ivy to download the client from Maven Central and then run it.

The source code for the Java client (ZanataClient) can be found here:
https://github.com/zanata/zanata-client/

See also our 0install option, which is a better choice in most cases: http://docs.zanata.org/projects/zanata-client/en/release/installation/linux-installation/


Fedora users don't need this (but this might be newer)
------------------------------------------------------

If you are using Fedora, you can just install `zanata-cli` through yum:

    $ sudo yum install zanata-client

You can keep zanata-cli up to date in the usual way (eg `yum update`).

However, if you aren't running the latest version of Fedora, the latest
version of the client may not be available, so you might want to try
the Ivy version (below).


Installing Ivy: on Fedora/RHEL
------------------------------

First, make sure you have Apache Ivy installed.  On Red Hat Enterprise Linux 6, you first need to enable EPEL, with a command like this:

    $ sudo rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm

Then install Ivy (this should work on Fedora too):

    $ sudo yum install -y apache-ivy


Installing Ivy: on other systems
--------------------------------

Download an [Ivy binary distribution](http://ant.apache.org/ivy/download.cgi), extract Ivy's jar file somewhere, and set the environment variable `IVY_JAR` to point to it.  For example:

    export IVY_JAR=~/apps/apache-ivy-2.4.0/ivy-2.4.0.jar


Installing zanata-cli (Ivy version)
-----------------------------------

Just save the script https://raw.github.com/zanata/zanata-client-ivy/master/zanata-cli somewhere on your path, and make sure it is executable.

For example, assuming you have `~/bin` in `$PATH`:

    cd ~/bin
    wget https://raw.github.com/zanata/zanata-client-ivy/master/zanata-cli
    chmod 755 zanata-cli

Note: It's a good idea to check for a new version of `zanata-cli` once in a while (especially when a new version of Zanata server is released).


Using zanata-cli (example)
--------------------------

    zanata-cli stats --url https://translate.example.com/ --project iok --project-version 6.4


Or if you have `zanata.xml` in the current directory:

    zanata-cli stats


Running development versions of zanata-cli
------------------------------------------

Each version of the script is mainly designed to work with a particular version of the Zanata client, but you can try using it with another version, eg the latest development version.

For example:

    export ZANATA_CLI_VERSION=3.9.0-SNAPSHOT
    zanata-cli help



Troubleshooting
---------------

If zanata-client-ivy has trouble resolving dependencies, try deleting the ivy cache:

    rm -rf ~/.ivy2/cache


Mailing list
------------

https://www.redhat.com/mailman/listinfo/zanata-users


Reporting bugs
--------------

Please report bugs in the Ivy client here:

https://zanata.atlassian.net/
