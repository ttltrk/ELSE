
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [M](https://github.com/ttltrk/ELSE/blob/master/M/M.MD) - [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

### UX Standard

---

```
history
```

```
less +<line_num> -N <file_name>

less +320 -N code.sh
```

```
ps -ef | grep file_name
```

```
nohup /path/path/code.sh &
```

```
cp file path
mv file path 
mv name new_name
```

```
unzip file_name
unzip -l file_name
gunzip file_name
```

```
chmod 777 file_dir
chown user:group file_name
chgrp groupname file_name
```

```
cat

--kiirja a file tartalmat
ttltrk-mbp:TEST attilatorok$ cat test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor

--megszamozva a sorokat kiirja a file tartalmat
ttltrk-mbp:TEST attilatorok$ cat -n test3.txt
     1	elso sor
     2	masodik sor
     3	harmadik sor
     4	negyedik sor es
     5	az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ 

--a harmadik sortol irja ki megszamozva a file tartalmat
ttltrk-mbp:TEST attilatorok$ cat -n test3.txt | more +3
     3  harmadik sor
     4  negyedik sor es
     5  az utolso otodik sor
     
--fileok tartalmat osszefuzi
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

```
head

--elso harom sor kiiratasa
ttltrk-mbp:TEST attilatorok$ head -3 test3.txt
elso sor
masodik sor
harmadik sor
ttltrk-mbp:TEST attilatorok$ 
```

```
more

--file tartalmat kiirja
ttltrk-mbp:TEST attilatorok$ more test3.txt
elso sor
masodik sor
harmadik sor
negyedik sor es
az utolso otodik sor

--file tartalmat kiirja a harmadik sortol
ttltrk-mbp:TEST attilatorok$ more +3 test3.txt
harmadik sor
negyedik sor es
az utolso otodik sor
```

```
sort

--sorokat rendez a fileon belul
ttltrk-mbp:TEST attilatorok$ sort test3.txt
az utolso otodik sor
elso sor
harmadik sor
masodik sor
negyedik sor es
ttltrk-mbp:TEST attilatorok$ 

--visszafele rendez
ttltrk-mbp:TEST attilatorok$ sort -r test3.txt
negyedik sor es
masodik sor
harmadik sor
elso sor
az utolso otodik sor
ttltrk-mbp:TEST attilatorok$ 
```

```
grep

--kiirja az a betus sorokat
ttltrk-mbp:TEST attilatorok$ grep a test3.txt
masodik sor
harmadik sor
az utolso otodik sor

--csak az a betus sorokat nem irja ki
ttltrk-mbp:TEST attilatorok$ grep -v a test3.txt
elso sor
negyedik sor es
ttltrk-mbp:TEST attilatorok$ 

--kiirja hogy egy keresett betu/szo/mondat hanyszor fordul elo a fileban
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

```
diff

--kiirja a ket file kozti kulonbseget
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

```
wc

--megszamolja a fileban a sorokat szavakat karaktereket
ttltrk-mbp:TEST attilatorok$ wc test3.txt
       5      13      71 test3.txt
ttltrk-mbp:TEST attilatorok$ 
       
--csak a sorokat szamolja meg       
ttltrk-mbp:TEST attilatorok$ wc -l test3.txt
       5 test3.txt
ttltrk-mbp:TEST attilatorok$ 
       
--csak a szavakat szamolja meg       
ttltrk-mbp:TEST attilatorok$ wc -w test3.txt
      13 test3.txt
ttltrk-mbp:TEST attilatorok$ 
      
--csak a karaktereket szamolja meg      
ttltrk-mbp:TEST attilatorok$ wc -c test3.txt
      71 test3.txt
ttltrk-mbp:TEST attilatorok$ 
```

```
tty

--kiirja az aktualis terminal nevet
ttltrk-mbp:TEST attilatorok$ tty
/dev/ttys000
ttltrk-mbp:TEST attilatorok$ 
```

---
