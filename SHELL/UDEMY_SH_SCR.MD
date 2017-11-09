
[Shell Scripting: Discover How to Automate Command Line](https://www.udemy.com/shell-scripting-linux/learn/v4/content)
======

### Start Here - Course Overview and Downloads
  * <a href='#1'>Course Overview</a>
  * <a href='#2'>Course Downloads</a>

### Shell Scripting, Succinctly
  * <a href='#3'>Section Introduction</a>
  * <a href='#4'>Shell Scripting, Part I</a>
  * <a href='#5'>Shell Scripting, Part II</a>
  * <a href='#6'>Quiz 1: Shell Scripting</a>
  * <a href='#7'>Practice Exercises</a>

### Exit Statuses and Return Codes
  * <a href='#8'>Exit Statuses and Return Codes</a>
  * <a href='#9'>Exit Status Demo</a>
  * <a href='#10'>Quiz 2: Exit Statuses and Return Codes</a>
  * <a href='#11'>Practice Exercises</a>

### Section 4

### Section 5

### Section 6

### Section 7

### Section 8

### Section 9

### Section 10

### Section 11

### Section 12

Start Here - Course Overview and Downloads
------

#### <h4 id='1'>Course Overview</h4>

#### <h4 id='2'>Course Downloads</h4>

Shell Scripting, Succinctly
------

#### <h4 id='3'>Section Introduction</h4>

#### <h4 id='4'>Shell Scripting, Part I</h4>

```shell
echo "Scripting is fun!"

>>>
Scripting is fun!
>>>
```

```shell
MY_SHELL="bash"
echo "I like the $MY_SHELL shell."

>>>
I like the bash shell.
>>>
```

```shell
MY_SHELL="bash"
echo "I like the ${MY_SHELL} shell."

>>>
I like the bash shell.
>>>
```

```shell
SERVER_NAME=(hostname)
echo "You are running this script on ${SERVER_NAME}."

>>>
You are running this script on hostname.
>>>
```

#### <h4 id='5'>Shell Scripting, Part II</h4>

```shell
if [ condition-is-true ]
then
  command 1
  command 2
  command N
fi
```

```shell
MY_SHELL="bash"

if [ "MY_SHELL" = "bash" ]
then
  echo "You seem to like the bash shell."
fi

>>>
You seem to like the bash shell.
>>>
```

```shell
if [ condition-is-true ]
then
  command N
else 
  command N
fi
```

```shell
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

```shell
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

```shell
for VARIABLE_NAME in ITEM_1 ITEM_N
do
  command 1
  command 2
  command N
done
```

```shell
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

```shell
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

```shell
USER=$1 # The first parameter is the user.
```

```shell
# Positional parameters are

$0, $1, $2, ... $9
$@
>>>
```

#### <h4 id='6'>Quiz 1: Shell Scripting</h4>

#### <h4 id='7'>Practice Exercises</h4>

Exit Statuses and Return Codes
------

#### <h4 id='8'>EXIT Statuses and Return Codes</h4>

```shell
HOST="http://google.com"

ping -c 1 $HOST

if [ "$?" -eq "0" ]
then
  echo "$HOST reachable."
else
  echo "$HOST unreachable."
fi

>>>
bash: ping: command not found
http://google.com unreachable.
>>>
```

```shell
HOST="http://google.com"

ping -c 1 $HOST

if [ "$?" -ne "0" ]
then
  echo "$HOST unreachable."
fi

>>>
bash: ping: command not found
http://google.com unreachable.
>>>
```

AND  ```&&```

OR ```||```

```shell
cp text.txt /tmp/bak ; cp test.txt /tmp

#Same as:

cp test.txt /tmp/bak
cp.test.txt /tmp
```

#### <h4 id='9'>Exit Status Demo</h4>

#### <h4 id='10'>Quiz 2: Exit Statuses and Return Codes</h4>

#### <h4 id='11'>Practice Exercises</h4>

