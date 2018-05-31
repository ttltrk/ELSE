
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [most used manuals](https://github.com/ttltrk/PRG/blob/master/MUM.MD) - [Unix](https://github.com/ttltrk/ELSE/blob/master/SHELL/OUM/OUM.MD) - [Courses](https://github.com/ttltrk/ELSE/blob/master/SHELL/OUM/COURSES/COURSES.MD) - [Udemy](https://github.com/ttltrk/ELSE/blob/master/SHELL/OUM/COURSES/UDEMY/UDEMY.MD)

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Operating System](https://github.com/ttltrk/ELSE/blob/master/BMOS/BMOS.MD)


###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [Operating System](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/12/OS.MD)

---

### Shell Scripting: Discover How to Automate Command Line

---

* [01 - Start Here - Course Overview and Downloads](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/01/01.MD)
* [02 - Shell Scripting, Succinctly](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/02/01.MD)
* [03 - Exit Statuses and Return Codes](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/03/01.MD)
* [04 - Functions](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/04/01.MD)
* [05 - Shell Script Checklist and Template](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/05/01.MD)
* [06 - Wildcards](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/06/01.MD)
* [07 - Case Statements](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/07/01.MD)
* [08 - Logging](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/08/01.MD)
* [09 - While Loops](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/09/01.MD)
* [10 - Debugging](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/10/01.MD)
* [11 - Scripts Used to Create This Course](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/11/01.MD)
* [12 - Slides](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/12/01.MD)
* [13 - Bonus Lecture Section: Get my other courses at the maximum discount!](https://github.com/ttltrk/ELSE/blob/master/SHELL/SH_SCR/13/01.MD)

---

### Exit Statuses and Return Codes
  * <a href='#8'>Exit Statuses and Return Codes</a>
  * <a href='#9'>Exit Status Demo</a>
  * <a href='#10'>Quiz 2: Exit Statuses and Return Codes</a>
  * <a href='#11'>Practice Exercises</a>

### Functions
  * <a href='#12'>Functions P-1</a>
  * <a href='#13'>Functions P-2</a>
  * <a href='#14'>Quiz 3: Functions</a>
  * <a href='#15'>Practice Exercises</a>
  * <a href='#16'>Review</a>

### Section 5

### Section 6

### Section 7

### Section 8

### Section 9

### Section 10

### Section 11

### Section 12

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

Functions
------

#### <h4 id='12'>Functions P-1</h4>

#### <h4 id='13'>Functions P-2</h4>

#### <h4 id='14'>Quiz 3: Functions</h4>

#### <h4 id='15'>Practice Exercises</h4>

#### <h4 id='16'>Review</h4>

