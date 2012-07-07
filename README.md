update-oracle-jvm
=================

Script for managing Oracle JVMs on Linux platforms (only tested debian).

Install
=======

1. Download [latest version](https://github.com/downloads/kengu/update-oracle-jvm/update-oracle-jvm-0.1.bin)
```
wget +x https://github.com/downloads/kengu/update-oracle-jvm/update-oracle-jvm-0.1.bin
```
2. Make binary executable
```
chmod +x update-oracle-jvm-*.bin
```
3. Install update-oracle-jvm
```
./update-oracle-jvm-*.bin
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

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/docs/help.png)

Acknowledgements
================

The self-extracting package is based on [Bash Self-Extracting Script](http://www.linuxjournal.com/node/1005818).