Zanata Java client script
-------------------------

Java command-line client for Zanata.

This repository doesn't include the actual Java code, just a shell script which uses
Ivy to download the client from Maven Central and then run it.

The source code for the Java client (ZanataClient) can be found here:
https://github.com/zanata/zanata-client/


Fedora users don't need this
----------------------------

If you are using Fedora, you don't need this version, you can just install `zanata-cli` through yum:

    $ sudo yum install zanata-client

You can keep zanata-cli up to date in the usual way (eg `yum update`).

However, if you aren't running the latest version of Fedora, the latest
version of the client may not be available, so you might want to try
the Ivy version (below).


Installing Ivy
--------------

First, make sure you have Apache Ivy installed.  On Red Hat Enterprise Linux 6, you first need to enable EPEL, with a command like this:

    $ sudo rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm

Then install Ivy (this should work on Fedora too):

    $ sudo yum install -y apache-ivy


Installing zanata-cli (Ivy version)
-----------------------------------

Just save the script https://raw.github.com/zanata/zanata-client-ivy/master/zanata-cli somewhere on your path, and make sure it is executable.

For example, if you have `~/bin` in `$PATH`:

    cd ~/bin
    wget https://raw.github.com/zanata/zanata-client-ivy/master/zanata-cli
    chmod 755 zanata-cli

Note: It's a good idea to check for a new version of `zanata-cli` once in a while (eg when a new version of Zanata server is released).


Using zanata-cli (example)
--------------------------

    zanata-cli stats --url https://translate.example.com/ --project iok --project-version 6.4


Or if you have `zanata.xml` in the current directory:
    zanata-cli stats


Troubleshooting
---------------

If zanata-client-ivy has trouble resolving dependencies, try deleting the ivy cache:

    rm -rf ~/.ivy2/cache


Reporting bugs
--------------

Please report bugs in the Ivy client here:

https://bugzilla.redhat.com/enter_bug.cgi?format=guided&product=Zanata&component=Component-zanata-client-ivy

