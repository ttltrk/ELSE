
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD)

###### [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [JV](https://github.com/ttltrk/PRG/blob/master/JAVA/JAVA.MD) - [C](https://github.com/ttltrk/PRG/blob/master/C/C.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [SH](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD) - [PL](https://github.com/ttltrk/PRG/blob/master/PERL/PL.MD) - [DS](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DS.MD) || [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) - [DE](https://github.com/ttltrk/ELSE/blob/master/LAN/GER/DUO_GER.MD) - [SP](https://github.com/ttltrk/ELSE/blob/master/LAN/SP/SP.MD) - [TR](https://github.com/ttltrk/ELSE/blob/master/LAN/TR/TR.MD) - [ESP](https://github.com/ttltrk/ELSE/blob/master/LAN/ESP/ESP.MD) || [Tools](https://github.com/ttltrk/ELSE/blob/master/M/TOOLS/TOOLS.MD)

---

<h3 id='^'>UX - Shell scripts</h3>

---

* <a href='#hw'>hello world</a></br>
* <a href='#arexp'>arithmetic expression</a></br>
* <a href='#userinput'>user input</a></br>
* <a href='#functions'>functions</a></br>
* <a href='#ifelse'>if-else</a></br>
* <a href='#for'>for</a></br>
* <a href='#while'>while</a><br>
* <a href='#arrays'>arrays</a></br>
* <a href='#file'>file</a></br>

---

<h3 id='hw'>hello world</h3>

```sh
echo "hello world"

>>>
hello world
>>>
```

```sh
echo "Scripting is fun!"

>>>
Scripting is fun!
>>>
```

```sh
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

```
echo "\"Linux is awesome"\"

>>>
"Linux is awesome"
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='arexp'>arithmetic expression</h3>

```
let val=500/2

echo $val

>>>
250
>>>
```

```
let val=500/2

val2=`echo $val`
echo $val2

>>>
250
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='userinput'>user input</h3>

```sh
echo "pls enter your name"
read name
echo "hi" $name

>>>
pls enter your name
trk
hi trk
>>>
```

```sh
read varname #Dan
echo Welcome $varname

#>>>
#Welcome Dan
#>>>
```

```sh
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
```

```sh
read a

val1=`echo "$a" | bc -l`
a_rounded=`printf "%.3f" $val1`

echo $a_rounded
```

<a href='#^'>^^^</a>

---

<h3 id='ifelse'>if-else</h3>

```
-eq equal
-ne not equal
-gt greather than
-lt less than
-gte greather than or equal
-lte less than or equal
```

```sh
if [ condition-is-true ]
then
  command 1
  command 2
  command N
fi
```

```sh
MY_SHELL="bash"

if [ "$MY_SHELL" = "bash" ]
then
  echo "You seem to like the bash shell."
fi

>>>
You seem to like the bash shell.
>>>
```

```sh
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

```sh
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

```sh
var1=10
var2=-10

if [ "$var1" -gt 0 ]; then; echo "YES"; else; echo "NO"; fi
if [ "$var2" -gt 0 ]; then; echo "YES"; else; echo "NO"; fi

>>>
YES
NO
>>>
```

```sh
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

```sh
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

<a href='#^'>^^^</a>

---

<h3 id='for'>for</h3>

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

```sh
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
```

<a href='#^'>^^^</a>

---

<h3 id='while'>while</h3>

```sh
input=""
while [[ $input != 'Y' ]]; do
    echo -n "Please enter Y to continue"
    read input
done

>>>
-n Please enter Y to continue
bbb
-n Please enter Y to continue
Y
>>>
```

Infinite loop in the background + logging

```sh
#!/usr/bin/env bash
while true; do
    echo `date` >> time.txt
    sleep 1
done

./infinite_loop_background.sh &
jobs
ps -ef | grep *loop*
tail -f time.txt
```

<a href='#^'>^^^</a>

---

<h3 id='arrays'>arrays</h3>

```sh
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
```

<a href='#^'>^^^</a>

---

<h3 id='function'>function</h3>


```sh
function usage {
	echo "hi trk"
}

usage

>>>
hi trk
>>>
```

```
username="trk"
echo $username
function proc {
  echo $username "from inside the func"
}
proc

>>>
$ ./ttt.sh
trk
trk from inside the func
$
>>>
```

```
username="trk"
echo $username
function proc {
  local username="at"
  echo $username "from inside the func"
}
proc

>>>
$ ./ttt.sh
trk
at from inside the func
$
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='file'>file</h3>

```sh
-d directory - dirctory exists
-e file - file exists
-f file - file exist and its a regular file
-r file - file is readable
-s file - file is not empty
-w file - file is writable
```

<a href='#^'>^^^</a>

---



