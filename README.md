Zanata Java client script
-------------------------

Java command-line client for Zanata.

This repository doesn't include the actual Java code, just a shell script which uses
Ivy to download the client from Maven Central and then run it.

The source code for the Java client (ZanataClient) can be found here:
https://github.com/zanata/zanata-client/


Installation
------------

Just save the script https://raw.github.com/zanata/zanata-cli-ivy/master/zanata-cli somewhere on your path, and make sure it is executable.

For example, if you have ~/bin in $PATH:

    cd ~/bin
    wget https://raw.github.com/zanata/zanata-cli-ivy/master/zanata-cli
    chmod 755 zanata-cli


Example command line
---------------------
    ./zanata-cli stats --url https://translate.example.com/ --project iok --project-version 6.4


If you have a zanata.xml in the current directory:
    ./zanata-cli stats

