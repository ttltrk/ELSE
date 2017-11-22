
[Fundamentals of Unix and Linux System Administration](https://www.udemy.com/fundamentals-of-unix-and-linux-system-administration/learn/v4/content)
======

### Introduction
  * <a href="#1">Introduction</a>

### Where to Start
  * <a href="#2">Linux Unix Administration Fundamentals</a>
  * <a href="#3">Getting help on Linux</a>
  * <a href="#4">Advance man command</a>
  * <a href="#5">Quiz 1: Section 1</a>

### Package Management
  * <a href="#6">Introduction to package management</a>
  * <a href="#7"></a>
  * <a href="#8"></a>
  * <a href="#9"></a>
  * <a href="#10"></a>
  * <a href="#11"></a>

### Section 4

### Section 5

### Section 6

### Section 7

### Section 8

### Section 9

### Section 10

### Section 11

### Section 12

### Section 13

### Section 14

### Section 15

### Section 16

### Section 17

### Section 18

### Section 19

### Section 20

### Section 21

### Section 22

### Section 23

### Section 24

Introduction
------

<h3 id="1">Introduction</h3>

Where to Start
------

<h3 id="2">Linux Unix Administration Fundamentals</h3>

<h3 id="3">Getting help on Linux</h3>

Moving in ```man``` file

```space``` down

```b``` back or up

```/``` search

```q``` exit

<h3 id="4">Advance man command</h3>


```which``` shows the full path of (shell) commands

```
which python

ttltrk-mbp:Desktop attilatorok$ which python
/usr/bin/python
ttltrk-mbp:Desktop attilatorok$ 
``` 

```history``` you can check the history about your used commands

```
HISTTIMEFORMAT="%d/%m/%y %T "
history

ttltrk-mbp:Desktop attilatorok$ HISTTIMEFORMAT="%d/%m/%y %T "
ttltrk-mbp:Desktop attilatorok$ history
  535  21/11/17 14:12:36 pwd
  536  21/11/17 14:12:45 more full_or_not
  537  21/11/17 14:12:50 pwd
  538  21/11/17 14:12:52 ls -l
  539  21/11/17 14:13:11 more full_or_not.html
  540  21/11/17 14:13:28 echo > full_or_not.html
  541  21/11/17 14:13:39 more full_or_not.html
  542  21/11/17 14:19:29 clear
  543  21/11/17 14:19:32 HISTTIMEFORMAT="%d/%m/%y %T "
  544  21/11/17 14:19:35 history
ttltrk-mbp:Desktop attilatorok$ 
```

```du``` estimate file space usage

```
du -h -d=1 *

ttltrk-mbp:Desktop attilatorok$ du -h -d=1 *
 74M	Brackets.Release.1.11.dmg
236M	Processing.app
9.7M	TheSpaGuiToProCreIntArtWitCod
120M	WEB
3.5M	course-e-book-web-v2.1 copy.pdf
3.5M	course-e-book-web-v2.1.pdf
3.4G	desk
109M	processing-3.3.6-macosx.zip
232K	ttltrk
ttltrk-mbp:Desktop attilatorok$ 
```

```
echo > full_or_not.html

ttltrk-mbp:Desktop attilatorok$ more full_or_not.html
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  <meta http-equiv="Content-Style-Type" content="text/css">
  <title></title>
  <meta name="Generator" content="Cocoa HTML Writer">
  <meta name="CocoaVersion" content="1404.47">
  <style type="text/css">
    p.p1 {margin: 0.0px 0.0px 0.0px 0.0px; font: 12.0px Helvetica}
  </style>
</head>
<body>
<p class="p1">full</p>
</body>
</html>
ttltrk-mbp:Desktop attilatorok$ 
ttltrk-mbp:Desktop attilatorok$ echo > full_or_not.html
ttltrk-mbp:Desktop attilatorok$ more full_or_not.html

ttltrk-mbp:Desktop attilatorok$ 
```

[linux.org](https://www.linux.org/)

[kernel.org](https://www.kernel.org/)

[serverfault.com](https://serverfault.com/)

### <h3 id="5">Quiz 1: Section 1</h3>

Package Management
------

### <h3 id="6">Introduction to package management</h3>

```tar``` tape archiver (Create, extract, or list files from a tar file)

```
tar -xvf <file_name>
```

```./configure``` A configure script is an executable script designed to aid in developing
a program to be run on a wide number of different computers. It matches the libraries
on the user's computer, with those required by the program before compiling it from its source code.

Package types

```RPM``` Red Hat Package

Install

```
rpmi -i <package_name.rpm>
```

Update

```
rpm - U <package_name.rpm>
```

```DEB``` Debian PKG used by Ubuntu
