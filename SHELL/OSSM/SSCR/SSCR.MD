
---

###### [MUM](https://github.com/ttltrk/PRG/blob/master/MUM.MD) || [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) || [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

<h3 id='^'>UX - Shell scripts</h3>

---

* <a href='#echo'>echo</a>
* <a href='#firstscript'>first script</a>
* <a href='#variables'>variables</a>
* <a href='#array'>Array</a>

<a href='#^'>^^^</a>

---

<h3 id='echo'>SS Echo</h3>

```bash
echo "Scripting is fun!"

>>>
Scripting is fun!
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='firstscript'>first script</h3>

```bash
[/home/TTLTRK] # echo '#!/bin/sh' > my-script.sh
[/home/TTLTRK] # echo 'echo Hello World' >> my-script.sh
[/home/TTLTRK] # ls -l
total 104
-rwxrwxrwx    1 TTLTRK   staff           152 Feb  4 01:57 c.sh
-rwxrwxrwx    1 TTLTRK   staff           114 Feb  4 01:46 ccc.sh
drwx------    2 TTLTRK   staff           256 Feb  4 01:43 first
-rw-------    1 TTLTRK   staff            27 Feb 20 08:04 my-script.sh
drwx------    2 TTLTRK   staff           256 Feb  4 01:44 second
[/home/TTLTRK] # chmod 775 my-script.sh
[/home/TTLTRK] # ./my-script.sh
Hello World
[/home/TTLTRK] #

or via vi

[b03cxnp09032:/home/TTLTRK] # vi first.sh

#!/bin/sh
# this is a comment
echo hello world  #this is a comment too

[/home/TTLTRK] # ls -l
total 112
-rwxrwxrwx    1 TTLTRK   staff           152 Feb  4 01:57 c.sh
-rwxrwxrwx    1 TTLTRK   staff           114 Feb  4 01:46 ccc.sh
drwx------    2 TTLTRK   staff           256 Feb  4 01:43 first
-rw-------    1 TTLTRK   staff            72 Feb 20 08:07 first.sh
-rwxrwxr-x    1 TTLTRK   staff            27 Feb 20 08:04 my-script.sh
drwx------    2 TTLTRK   staff           256 Feb  4 01:44 second
[/home/TTLTRK] # chmod 755 first.sh
[/home/TTLTRK] # ./first.sh
hello world
[/home/TTLTRK] # cat first.sh
#!/bin/sh
# this is a comment
echo hello world  #this is a comment too
[/home/TTLTRK] #

```

---
  
<h3 id='variables'>SS Variables</h3>

```bash
MY_SHELL="bash"
echo "I like the $MY_SHELL shell."

>>>
I like the bash shell.
>>>
```

<a href='#^'>^^^</a>

```bash
MY_SHELL="bash"
echo "I like the ${MY_SHELL} shell."

>>>
I like the bash shell.
>>>
```

<a href='#^'>^^^</a>

```bash
SERVER_NAME=(hostname)
echo "You are running this script on ${SERVER_NAME}."

>>>

>>>
```

<a href='#^'>^^^</a>

---

<h3 id='array'>SS Array</h3>

```bash
first()
  {  
   jjj="TRK"
   arr=("jjj" "$jjj")
   
   for i in "${arr[@]}"
   do
     echo "$i" 
   done
  }

first 

>>>
jjj
TRK
>>>
```

<a href='#^'>^^^</a>

---
