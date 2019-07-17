
---

###### [MUM](https://github.com/ttltrk/PRG/blob/master/MUM.MD) || [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) || [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

<h3 id='^'>UX - Shell scripts</h3>

---

```bash
echo "first line"; echo "second line"
echo "third line"
echo "fourth line"

>>>
first line
second line
third line
fourth line
>>>
```

<a href='#^'>^^^</a>

```bash
var1=10
var2=-10

if [ "$var1" -gt 0 ]; then; echo "YES"; else; echo "NO"; fi
if [ "$var2" -gt 0 ]; then; echo "YES"; else; echo "NO"; fi

>>>
YES
NO
>>>
```

<a href='#^'>^^^</a>

---

```bash
read ch

if [ $ch = 'y' ]
then
    echo "YES"
elif [ $ch = 'Y' ]
then
    echo "YES"
elif [ $ch = 'n' ]
then
    echo "NO"
elif [ $ch = 'N' ]
then
    echo "NO"

fi
```

```bash
read n1
read n2
read n3

if (( $n1 == $n2 && $n2 == $n3 && $n1 == $n3 ))
then
    echo "EQUILATERAL  "
elif (( $n1 == $n2 || $n1 == $n3 || $n3 == $n2 ))
then
    echo "ISOSCELES  "
elif (( $n1 + $n2 > $n3 && $n1 + $n3 > $n2 && $n2 + $n3 > $n1 ))
then
    echo "SCALENE"

fi
```

```bash
read a

val1=`echo "$a" | bc -l`
a_rounded=`printf "%.3f" $val1`

echo $a_rounded
```

<a href='#^'>^^^</a>

---

```bash

#------------------------------------------------------
#------------------------------------------------------

#echo

echo "Scripting is fun!"

#>>>
#Scripting is fun!
#>>>

#------------------------------------------------------
#------------------------------------------------------

# variables

MY_SHELL="bash"
echo "I like the $MY_SHELL shell."

#>>>
#I like the bash shell.
#>>>

#------------------------------------------------------
#------------------------------------------------------

# Array

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

#>>>
#jjj
#TRK
#>>>

#------------------------------------------------------
#------------------------------------------------------

#iteration

for number in {1..99..2}
do
    echo $number
done

#>
#1
#3
#5
#7
#.
#.
#.
#99
#>

#------------------------------------------------------
#------------------------------------------------------

#User input

read varname #Dan
echo Welcome $varname

#>>>
#Welcome Dan
#>>>

#------------------------------------------------------
#------------------------------------------------------

# +-*/

read a #5
read b #2
 
a1=$(( $a + $b ))
a2=$(( $a - $b ))
a3=$(( $a * $b ))
a4=$(( $a / $b ))
 
echo $a1
echo $a2
echo $a3
echo $a4

#>>>
#7
#3
#10
#2
#>>>

#------------------------------------------------------
#------------------------------------------------------

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

<a href='#^'>^^^</a>

---

```
echo "Scripting is fun!"

>>>
Scripting is fun!
>>>
```

```
VARIABLE_NAME="value"
MY_SHELL="bash"
echo "I like the $MY_SHELL shell."

>>>
I like the bash shell.
>>>
```

```
MY_SHELL="bash"
echo "I like the ${MY_SHELL} shell."

>>>
I like the bash shell.
>>>
```

```
SERVER_NAME=(hostname)
echo "You are running this script on ${SERVER_NAME}."

>>>
You are running this script on hostname.
>>>
```

<a href='#^'>^^^</a>

---

```
if [ condition-is-true ]
then
  command 1
  command 2
  command N
fi
```

```
MY_SHELL="bash"

if [ "$MY_SHELL" = "bash" ]
then
  echo "You seem to like the bash shell."
fi

>>>
You seem to like the bash shell.
>>>
```

```
if [ condition-is-true ]
then
  command N
else 
  command N
fi
if [ condition-is-true ]
then
  command N
elif [ condition-is-true ]
then
  command N
else
  command N
fi
```

```
MY_SHELL="csh"

if [ "$MY_SHELL" = "bash" ]
then
  echo "You seem to like the bash shell."
elif [ "$MY_SHELL" = "csh" ]
then
  echo "You seem to like the csh shell."
else
  echo "You don't seem to like the bash or csh shells."
fi

>>>
You seem to like the csh shell.
>>>
```

```
for VARIABLE_NAME in ITEM_1 ITEM_N
do
  command 1
  command 2
  command N
done
```

```bash
color="red green blue"

echo $color

>>>
red green blue
>>>
```

```bash
for COLOR in red green blue
do
  echo "COLOR: $COLOR"
done

>>>
COLOR: red
COLOR: green
COLOR: blue
>>>
```

```
COLORS="red green blue"

for COLOR in $COLORS
do
  echo "COLOR: $COLOR"
done

>>>
COLOR: red
COLOR: green
COLOR: blue
>>>
```

```
USER=$1 # The first parameter is the user.
# Positional parameters are

$0, $1, $2, ... $9
$@
>>>
````

<a href='#^'>^^^</a>

---
