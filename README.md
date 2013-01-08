Zanata Java client script
-------------------------

Java command-line client for Zanata.

This repository doesn't include the actual Java code, just a shell script which uses
Ivy to download the client from Maven Central and then run it.

The source code for the Java client (ZanataClient) can be found here:
https://github.com/zanata/zanata-client/



Example command line
---------------------
    zanataj stats --url https://translate.example.com/ --project iok --project-version 6.4


If you have a zanata.xml in the current directory:
    zanataj stats

