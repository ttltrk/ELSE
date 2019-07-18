
---

###### [MUM](https://github.com/ttltrk/PRG/blob/master/MUM.MD) || [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) || [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

<h3 id='^'>UX - Standard</h3>

---

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
* <a href='#tty'>tty</a></br>
* <a href='#unzip'>unzip</a></br>
* <a href='#wc'>wc</a></br>

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
nohup /path/path/code.sh &
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

