
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD)

###### [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [JV](https://github.com/ttltrk/PRG/blob/master/JAVA/JAVA.MD) - [C](https://github.com/ttltrk/PRG/blob/master/C/C.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [SH](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD) - [PL](https://github.com/ttltrk/PRG/blob/master/PERL/PL.MD) - [DS](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DS.MD) - [DO](https://github.com/ttltrk/ELSE/blob/master/DOCKER/DOCKER/DOCKER.MD) || [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) - [DE](https://github.com/ttltrk/ELSE/blob/master/LAN/GER/DUO_GER.MD) - [SP](https://github.com/ttltrk/ELSE/blob/master/LAN/SP/SP.MD) - [FR](https://github.com/ttltrk/ELSE/blob/master/LAN/FR/FR.MD) - [TR](https://github.com/ttltrk/ELSE/blob/master/LAN/TR/TR.MD) - [LA](https://github.com/ttltrk/ELSE/blob/master/LAN/LATIN/LATIN.MD) - [ESP](https://github.com/ttltrk/ELSE/blob/master/LAN/ESP/ESP.MD) || [Tools](https://github.com/ttltrk/ELSE/blob/master/M/TOOLS/TOOLS.MD)

---

<h3 id='^'>UX - Standard</h3>

---

* <a href='#alias'>alias</a></br>
* <a href='#cat'>cat</a></br>
* <a href='#chgrp'>chgrp</a></br>
* <a href='#clear'>clear</a></br>
* <a href='#chmod'>chmod</a></br>
* <a href='#chown'>chown</a></br>
* <a href='#cmp'>cmp</a></br>
* <a href='#comm'>comm</a></br>
* <a href='#cp'>cp</a></br>
* <a href='#diff'>diff</a></br>
* <a href='#du'>du</a></br>
* <a href='#echo'>echo</a></br>
* <a href='#grep'>grep</a></br>
* <a href='#head'>head</a></br>
* <a href='#history'>history</a></br>
* <a href='#less'>less</a></br>
* <a href='#ln'>ln</a></br>
* <a href='#ls'>ls</a></br>
* <a href='#more'>more</a></br>
* <a href='#mv'>mv</a></br>
* <a href='#nohup'>nohup</a></br>
* <a href='#passwd'>passwd</a></br>
* <a href='#ps'>ps</a></br>
* <a href='#sort'>sort</a></br>
* <a href='#tail'>tail</a></br>
* <a href='#touch'>touch</a></br>
* <a href='#tty'>tty</a></br>
* <a href='#unzip'>unzip</a></br>
* <a href='#wc'>wc</a></br>

---

<h3 id='alias'>alias</h3>

```sh
$ la
la: not found
$
$ alias la="ls -la"
$ la

>
.
.
.
.
>
```

<a href='#^'>^^^</a>

---

<h3 id='cat'>cat</h3>

kiirja a file tartalmat

```
cat file_name.txt

ttltrk-mbp:TEST attilatorok$ cat test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor
```

szamozva kiirja a file tartalmat

```
cat -n file_name.txt

ttltrk-mbp:TEST attilatorok$ cat -n test3.txt
     1	elso sor
     2	masodik sor
     3	harmadik sor
     4	negyedik sor es
     5	az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ 
```

szamozva kiirja a file tartalmat a 3.ik sortol

```
cat -n file_name.txt | more +3

ttltrk-mbp:TEST attilatorok$ cat -n test3.txt | more +3
     3  harmadik sor
     4  negyedik sor es
     5  az utolso otodik sor
```

fileok tartalmat (1-2) osszefuzi (a 3.ik-ba)

```
cat file_name_1.txt file_name_2.txt > file_name_3.txt

ttltrk-mbp:TEST attilatorok$ cat t1.txt
t1 - elso sora
ttltrk-mbp:TEST attilatorok$ cat t2.txt
t2 - elso sora
t2 - masodik sora
ttltrk-mbp:TEST attilatorok$ cat t3.txt
:
ttltrk-mbp:TEST attilatorok$ cat t1.txt t2.txt > t3.txt
ttltrk-mbp:TEST attilatorok$ cat t3.txt
t1 - elso sora
t2 - elso sora
t2 - masodik sora
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='chgrp'>chgrp</h3>

```
chgrp groupname file_name
```

<a href='#^'>^^^</a>

---

<h3 id='clear'>clear</h3>

clear the whole screen

```
clear
```

<a href='#^'>^^^</a>

---

<h3 id='chmod'>chmod</h3>

```
chmod 777 file_dir
```

<a href='#^'>^^^</a>

---

<h3 id='chown'>chown</h3>

```
chown user:group file_name
```

<a href='#^'>^^^</a>

---

<h3 id='cmp'>cmp</h3>

```
$ cat temp.txt
this is some other text
this is appended text
$ cat temp2.txt
temp2 temp2
this is some other text
this is appended text
$ cmp temp.txt temp2.txt
temp.txt temp2.txt differ: char 2, line 1
$
```

<a href='#^'>^^^</a>

---

<h3 id='comm'>comm</h3>

```
$ cat temp.txt
this is some other text
this is appended text
$
$ cat temp2.txt
temp2 temp2
this is some other text
this is appended text
$
$ comm -1 temp.txt temp2.txt
temp2 temp2
        this is some other text
        this is appended text
$ comm -2 temp.txt temp2.txt
        this is some other text
        this is appended text
$ comm -12 temp.txt temp2.txt
this is some other text
this is appended text
$
```

<a href='#^'>^^^</a>

---

<h3 id='cp'>cp</h3>

```
cp file path
```

<a href='#^'>^^^</a>

---

<h3 id='diff'>diff</h3>

kiirja ket file kozotti kulonbseget

```
diff file_name_1.txt file_name_2.txt

ttltrk-mbp:TEST attilatorok$ cat test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ cat test4.txt
elso sor
masodik sor
harmadik sor
az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ diff test3.txt test4.txt
4d3
< negyedik sor es
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='du'>du</h3>

```
$ du
         6 ./DELTA
         2 ./dos2unix
  25033830 ./EXP_PRD/trk/nonstage
   2165384 ./EXP_PRD/trk/nonstage_new
  27199215 ./EXP_PRD/trk
  27199216 ./EXP_PRD
         8 ./HR
     11447 ./MILOS EXP
      1587 ./sanity_checks/monthly_bundling
      1705 ./sanity_checks/weekly_bundling
      3293 ./sanity_checks
  27214487 .
$
```

```
$ du -h
    3.00KB ./DELTA
    1.00KB ./dos2unix
   11.94GB ./EXP_PRD/trk/nonstage
    1.03GB ./EXP_PRD/trk/nonstage_new
   12.97GB ./EXP_PRD/trk
   12.97GB ./EXP_PRD
    4.00KB ./HR
    5.59MB ./MILOS EXP
  793.50KB ./sanity_checks/monthly_bundling
  852.50KB ./sanity_checks/weekly_bundling
    1.61MB ./sanity_checks
   12.98GB .
$
```

```
$ du -h DOCS
   43.50KB DOCS/OWN
   14.95MB DOCS/PY3/1-50
   16.26MB DOCS/PY3/101-150
   16.05MB DOCS/PY3/151-200
   17.11MB DOCS/PY3/201-250
   16.49MB DOCS/PY3/251-300
   15.97MB DOCS/PY3/301-350
   16.18MB DOCS/PY3/51-100
  113.01MB DOCS/PY3
  160.65MB DOCS
$
```

```
[blabla:/home/xxx] # find  /bla/bla/bla/ -mtime +365 | wc -l 
     166

van 166 olyan 2M fájlunk, ami egy éve ott van

[blabla:/home/xxx] # du -g //bla/bla/bla/
31.85   //bla/bla/bla/

32Giga van benne jelenleg


[blabla:/blabla/blabla/blabla] # df -g /dev/lv_bbb
Filesystem    GB blocks      Free %Used    Iused %Iused Mounted on
/dev/lv_bbb     675.00    219.57   68%   242099     1% /mclm
[blabla:/blabla/blabla/blabla] #
```

<a href='#^'>^^^</a>

---

<h3 id='echo'>echo</h3>

create/update a file

```
echo "this is some text" > temp.txt
cat temp.txt

>>>
this is some text
>>>

echo "this is some other text" > temp.txt
cat temp.txt

>>>
this is some other text
>>>
```

Append a text

```
echo "this is appended text" >> temp.txt
cat temp.txt

>>>
this is some other text
this is appended text
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='grep'>grep</h3>

how to find errors in the log files

```sh
$ ls -l log*.txt
-rwxrwxrwa   1 AzureAD\AttilaTorok AzureAD\AttilaTorok      78 Jul 23 14:03 log.txt
-rwxrwxrwa   1 AzureAD\AttilaTorok AzureAD\AttilaTorok      31 Jul 23 14:02 log2.txt
$
$ cat log.txt
hi
sec lne
third line 4th line
error - 4
5th line
sixth line
error - 7
$ cat log2.txt
abort - 1
hi
abort - 3
$ ttt.sh
log.txt:error - 4
log.txt:error - 7
log2.txt:abort - 1
log2.txt:abort - 3
$ cat ttt.sh
grep error log*.txt
grep abort log*.txt
```

```sh
$ cat ttt.sh
echo "pls enter your name"
read name
echo "hi" $name$
$
$ grep echo ttt.sh
echo "pls enter your name"
echo "hi" $name
$
$ grep read ttt.sh
read name
$
```

kiirja az 'a' betus sorokat

```
grep a file_name.txt

ttltrk-mbp:TEST attilatorok$ grep a test3.txt
masodik sor
harmadik sor
az utolso otodik sor
```

csak az 'a' betus sorokat nem irja ki

```
grep -v a file_name.txt

ttltrk-mbp:TEST attilatorok$ grep -v a test3.txt
elso sor
negyedik sor es
ttltrk-mbp:TEST attilatorok$ 
```

kiirja hogy egy keresett betu/szo/mondat hanyszor fordul elo a fileban

```
grep -c <word> file_name.txt
grep -c <char> file_name.txt
grep -c 'example sentence' file_name.txt

ttltrk-mbp:TEST attilatorok$ cat test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ grep -c sor test3.txt
5
ttltrk-mbp:TEST attilatorok$ grep -c elso test3.txt
1
ttltrk-mbp:TEST attilatorok$ grep -c u test3.txt
1
ttltrk-mbp:TEST attilatorok$ grep -c 'elso sor' test3.txt
1
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='head'>head</h3>

elso harom sor kiiratasa

```
head -3 file_name.txt

ttltrk-mbp:TEST attilatorok$ head -3 test3.txt
elso sor
masodik sor
harmadik sor
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='history'>history</h3>

```
history
```

<a href='#^'>^^^</a>

---

<h3 id='less'>less</h3>

```
less +<line_num> -N <file_name>

less +320 -N code.sh
```

<a href='#^'>^^^</a>

---

<h3 id='ln'>ln</h3>

Create a Symbolic link sudo ln -s <path> <name>

```
cd /var/www/html
pwd
/var/www/html
sudo ln -s /var/spool/apt-mirror ubuntu
```

<a href='#^'>^^^</a>

---

<h3 id='ls'>ls</h3>

```
ls -l
```

list out to the directory where the proc is running

```
ls -l /proc/<pid>/fd
```

list out all processes

```
ps -ef | grep <proc_name>
```

<a href='#^'>^^^</a>

---

<h3 id='more'>more</h3>

kiirja a file tartalmat

```
more file_name.txt

ttltrk-mbp:TEST attilatorok$ more test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor
```

kiirja a file tartalmat a 3.ik sortol

```
more +3 file_name.txt

ttltrk-mbp:TEST attilatorok$ more +3 test3.txt
harmadik sor
negyedik sor es
az utolso otodik sor
```

<a href='#^'>^^^</a>

---

<h3 id='mv'>mv</h3>

```
mv file path 
mv name new_name
```

<a href='#^'>^^^</a>

---

<h3 id='nohup'>nohup</h3>

```
nohup sh /path/path/code.sh &
```

check the nohup.out

```
tail -f nohup.out
```

<a href='#^'>^^^</a>

---

<h3 id='passwd'>passwd</h3>

change password

```
passwd
```

<a href='#^'>^^^</a>

---

<h3 id='ps'>ps</h3>

```
ps -ef | grep file_name
```

```
ps -ef | grep file_name | wc -l
```

count the lines without grep

```
$ ps -ef | grep http
AttilaTo  11640  14504  0 06:27:23 con  <blablabla> 0:00  --v=1
AttilaTo  14348   8484  0 06:29:37 con  <blablabla> 0:00  --annotation=ver
AttilaTo  18880   4116  0 14:48:42 con  0:00 grep http
$
$
$ ps -ef | grep http | wc -l
      3
$
$
$ ps -ef | grep http | grep -v grep | wc -l
      2
$
```

<a href='#^'>^^^</a>

---

<h3 id='sort'>sort</h3>

sorokat rendez a fileon belul

```
sort file_name.txt

ttltrk-mbp:TEST attilatorok$ sort test3.txt
az utolso otodik sor
elso sor
harmadik sor
masodik sor
negyedik sor es
ttltrk-mbp:TEST attilatorok$ 
```

visszafele rendez

```
sort -r file_name.txt

ttltrk-mbp:TEST attilatorok$ sort -r test3.txt
negyedik sor es
masodik sor
harmadik sor
elso sor
az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='tail'>tail</h3>

tail is a basic Unix command for quickly accessing the last few lines of a given text file. 
tail is particularly useful for working with log files.

```
tail -f <filename>
```

<a href='#^'>^^^</a>

---

<h3 id='touch'>touch</h3>

create 4 files

```
xxx:yyy:/home/TTLTRK/shell$ touch test1 test2 test3 test4
```

```
xxx:yyy:/home/TTLTRK/shell$ touch wood.txt
xxx:yyy:/home/TTLTRK/shell$ echo 'here is something, use it' > wood.txt
xxx:yyy:/home/TTLTRK/shell$ cat wood.txt
here is something, use it
xxx:yyy:/home/TTLTRK/shell$
```

```
xxx:yyy:/home/TTLTRK/shell$ echo 'the second line comes here' >> wood.txt
xxx:yyy:/home/TTLTRK/shell$ cat wood.txt
here is something, use it
the second line comes here
xxx:yyy:/home/TTLTRK/shell$
```

```
xxx:yyy:/home/TTLTRK/shell$ > wood.txt
xxx:yyy:/home/TTLTRK/shell$ cat wood.txt
xxx:yyy:/home/TTLTRK/shell$
```

<a href='#^'>^^^</a>

---

<h3 id='tty'>tty</h3>

kiirja az aktualis terminal nevet

```
tty

ttltrk-mbp:TEST attilatorok$ tty
/dev/ttys000
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

<h3 id='unzip'>unzip</h3>

```
unzip file_name
unzip -l file_name
gunzip file_name
```

<a href='#^'>^^^</a>

---

<h3 id='wc'>wc</h3>

megszamolja a filekot egy konyvtarban

```
ls -1 | wc -l
```

megszamolja a fileban a sorokat szavakat karaktereket

```
wc file_name.txt

ttltrk-mbp:TEST attilatorok$ wc test3.txt
       5      13      71 test3.txt
ttltrk-mbp:TEST attilatorok$ 
```

csak a sorokat szamolja meg       

```
wc -l file_name.txt

ttltrk-mbp:TEST attilatorok$ wc -l test3.txt
       5 test3.txt
ttltrk-mbp:TEST attilatorok$ 
```

csak a szavakat szamolja meg       

```
wc -w file_name.txt

ttltrk-mbp:TEST attilatorok$ wc -w test3.txt
      13 test3.txt
ttltrk-mbp:TEST attilatorok$ 
```

csak a karaktereket szamolja meg      

```
wc -c file_name.txt

ttltrk-mbp:TEST attilatorok$ wc -c test3.txt
      71 test3.txt
ttltrk-mbp:TEST attilatorok$ 
```

<a href='#^'>^^^</a>

---

