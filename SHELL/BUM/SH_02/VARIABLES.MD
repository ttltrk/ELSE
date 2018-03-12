
### Using Variables

---

[<<<](https://github.com/ttltrk/ELSE/blob/master/SHELL/BUM/BUM.MD)

---

* VARIABLE NAMES
* DEFINING VARIABLES
* ACCESSING VALUES
* READ-ONLY VARIABLES
* UNSETTING VARIABLES
* VARIABLE TYPES

---

VARIABLE NAMES

```
_ALI
TOKEN_A
VAR_1
VAR_2
```
---

DEFINING VARIABLE

```
NAME="TRK"
AGE=35
```

---

ACCESSING VALUES

```
NAME="TRK"
echo $NAME

>>>
TRK
>>>
```
---

READ ONLY VARIABLES

```
NAME="TRK"
readonly NAME
NAME="TTL"
```

---

UNSETTING VARIABLES

```
NAME="TRK"
unset NAME
echo $NAME

>>>

>>>
```

---

VARIABLE TYPES

* Local Variables - A local variable is a variable that is present within the current instance of the shell. It is not available to 
programs that are started by the shell. They are set at the command prompt.

* Environment Variables - An environment variable is available to any child process of the shell. Some programs need environment 
variables in order to function correctly. Usually, a shell script defines only those environment variables that are needed by the 
programs that it runs.

* Shell Variables - A shell variable is a special variable that is set by the shell and is required by the shell in order to function 
correctly. Some of these variables are environment variables whereas others are local variables.

---

[src](https://www.tutorialspoint.com/unix/unix-using-variables.htm)

---
