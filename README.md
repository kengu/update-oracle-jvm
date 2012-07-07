update-oracle-jvm
=================

Script for managing Oracle JVMs on Linux platforms (only tested on Ubuntu 12.04 LTS).

Install
=======

1. Download [latest version](https://github.com/downloads/kengu/update-oracle-jvm/update-oracle-jvm-0.3.bin)
```
wget https://github.com/downloads/kengu/update-oracle-jvm/update-oracle-jvm-0.3.bin
```
2. Make binary executable
```
chmod +x update-oracle-jvm-0.3.bin
```
3. Install update-oracle-jvm
```
./update-oracle-jvm-0.3.bin
```

Usage
=====

1. Download Oracle JVM(s) from http://www.oracle.com/technetwork/java/javase/downloads/
2. Run 
```
./update-oracle-jvm [OPTIONS] FILE
```

Documentation (option -h)
=========================

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/help.png?raw=true)

Acknowledgements
================

The self-extracting package is based on [Bash Self-Extracting Script](http://www.linuxjournal.com/node/1005818).
