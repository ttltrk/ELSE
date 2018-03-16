
---

### File Management

---

[<<<](https://github.com/ttltrk/ELSE/blob/master/SHELL/BUM/BUM.MD)

---

* <a href="">File Types</a>
* <a href="">Listing Files</a>
* <a href="">Metacharacters</a>
* <a href="">Hidden Files</a>
* <a href="">Creating Files</a>
* <a href="">Editing Files</a>
* <a href="">Display Content of a File</a>
* <a href="">Counting Words in a File</a>
* <a href="">Copying Files</a>
* <a href="">Renaming Files</a>
* <a href="">Deleting Files</a>
* <a href="">Standard Unix Streams</a>

---

<h3 id="">File Types</h3>

|File Type|Description|
|------|------|
|Ordinary Files|An ordinary file is a file on the system that contains data, text, or program instructions. In this tutorial, you look at working with ordinary files.|
|Directories| Directories store both special and ordinary files. For users familiar with Windows or Mac OS, Unix directories are equivalent to folders.|
|Special Files|Some special files provide access to hardware such as hard drives, CD-ROM drives, modems, and Ethernet adapters. Other special files are similar to aliases or shortcuts and enable you to access a single file using different names.|

---

<h3 id="">Listing Files</h3>

To list the files and directories stored in the current directory

```
ls
```

---

<h3 id="">Metacharacters</h3>

```
ls *.doc
```

---

<h3 id="">Hidden Files</h3>

Some common examples of the hidden files include the files

```
.profile − The Bourne shell ( sh) initialization script

.kshrc − The Korn shell ( ksh) initialization script

.cshrc − The C shell ( csh) initialization script

.rhosts − The remote shell configuration file
```

---

<h3 id="">Creating Files</h3>

```
vi <filename>

blabla

---

<h3 id="">Editing Files</h3>

```
vi <filename>
```

---

<h3 id="">Display Content of a File</h3>

```
cat <filename>
```

You can display the line numbers by using the ```-b``` option along with the ```cat``` command

```
cat -b <filename>
```

---

<h3 id="">Counting Words in a File</h3>

```
wc <filename>
```

```
wc <filename1> <filename2> <filename3>
```

---

<h3 id="">Copying Files</h3>

```
cp <source_file> <destination_file>
```

---

<h3 id="">Renaming Files</h3>

```
mv old_file new_file
```

```
mv filename newfile
```

---

<h3 id="">Deleting Files</h3>

```
rm <filename>
```

```
rm <filename1> <filename2> <filename3>
```

---

<h3 id="">Standard Unix Streams</h3>

|Stream|Description|
|---|---|
|stdin|This is referred to as the standard input and the associated file descriptor is 0. This is also represented as STDIN. The Unix program will read the default input from STDIN.|
|stdout|This is referred to as the standard output and the associated file descriptor is 1. This is also represented as STDOUT. The Unix program will write the default output at STDOUT|
|stderr|This is referred to as the standard error and the associated file descriptor is 2. This is also represented as STDERR. The Unix program will write all the error messages at STDERR.|

---

[src](https://www.tutorialspoint.com/unix/unix-file-management.htm)

---
