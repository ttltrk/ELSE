
---

###### [MUM](https://github.com/ttltrk/PRG/blob/master/MUM.MD) || [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) || [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

<h3 id='^'>UX - Shell scripts</h3>

---

* <a href='#basics'>basics</a></br>
* <a href='#userinput'>user input</a></br>
* <a href='#ifelse'>if-else</a></br>
* <a href='#for'>for</a></br>
* <a href='#arrays'>arrays</a></br>

---

<h3 id='basics'>basics</h3>

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


