update-oracle-jvm
=================

Script for managing Oracle JVMs on Linux platforms (only tested on Ubuntu 12.04 LTS).

Install
=======

1. Download [latest version](https://dl.dropbox.com/u/14738337/git/update-oracle-jvm-latest.bin)
```
wget https://dl.dropbox.com/u/14738337/git/update-oracle-jvm-latest.bin
```
2. Make binary executable
```
chmod +x update-oracle-jvm-latest.bin
```
3. Install update-oracle-jvm
```
./update-oracle-jvm-latest.bin
```

Usage
=====

1. Download Oracle JVM(s) from http://www.oracle.com/technetwork/java/javase/downloads/
2. Run 
```
update-oracle-jvm install [OPTIONS] FILE...
```

Documentation
=============

```bash
> update-oracle-jvm -h
```

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/help.png?raw=true)

```bash
> update-oracle-jvm help install
```

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/install.png?raw=true)

```bash
> update-oracle-jvm help remove
```

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/remove.png?raw=true)

```bash
> update-oracle-jvm help list
```

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/list.png?raw=true)

```bash
> update-oracle-jvm help set
```

![update-oracle-jvm-help](https://github.com/kengu/update-oracle-jvm/blob/master/docs/set.png?raw=true)

Acknowledgements
================

The self-extracting package is based on [Bash Self-Extracting Script](http://www.linuxjournal.com/node/1005818).
