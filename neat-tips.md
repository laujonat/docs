---
description: This section contains basic Linux commands I use daily.
---

# Basic Tips

#### List Files

#### `ls`

* `ls -lt` - Sort output by last date and time modified:
* `ls -halt`- Sort both hidden and human readable sizes

#### `df`

The df utility displays statistics about the amount of free disk space on the specified filesystem or on the filesystem of which file is a part.

* Human-readable output
  * `df -H` - Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte in order to reduce the number of digits to three or less using base 10
  * `df -h` - Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte.
  * `df -l` - Only display information about locally-mounted filesystems

**Source**

* [https://www.systutorials.com/docs/linux/man/1p-df/](https://www.systutorials.com/docs/linux/man/1p-df/)

### `du`

 Display disk usage for file, folder, directories

* `du -sh */`

### `du`

 Display disk usage for file, folder, directories

* `du -sh */`

### `awk`

```bash
NAME
awk - pattern-directed scanning and processing language

SYNOPSIS
awk [ -F fs ] [ -v var=value ] [ 'prog' | -f progfile ] [ file ... ]
```

* Awk scans each input file for lines that match any of a set of patterns specified literally in prog or in one or more files specified as `-f` profile.
* The `-F (fs)` option defines the input field separator to be the regular expression fs.
* Get hostname if you know Host, get Host if you know Hostname

```bash
awk -v h="172.31.98.85" '$1 == "Host" {r = $2} $1 == "Hostname" && $2 == h {print r; exit}' ~/.ssh/config
```

 **Source**

* [https://unix.stackexchange.com/questions/430550/split-single-line-into-multiple-lines-newline-character-missing-for-all-the-lin](https://unix.stackexchange.com/questions/430550/split-single-line-into-multiple-lines-newline-character-missing-for-all-the-lin)

### `sed`

 Stream editor that reads the specified files, or the standard input if no files are specified, modifying the input as specified by a list of commands.  


#### Show shell startup time

  
 `for i in $(seq 1 10); do /usr/bin/time $SHELL -i -c exit; done`  


