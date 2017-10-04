<html>
<head></head>
<body>
learnshell.org

01. Learn the Basics
  
  01.001. <a href="#01.001.">Hello World</a>
  01.002. <a href="#01.002.">Variables</a>
  01.003. Passing Arguments to the Script
  01.004. Arrays
  01.005. Basic Operators
  01.006. Basic String Operations
  01.007. Decision Making
  01.008. Loops
  01.009. Shell Functions

02. Advanced Tutorials

03. Contributing Tutorials


01. Learn the Basics

<h2 id="01.001.">01.001. Hello World</h2>

The tutorial discusses shell programming in general with focus on Bash ("Bourne Again Shell") 
shell as the main shell interpreter. Shell programming using other common shells such as sh, csh, tcsh, 
will also be referenced, as they sometime differ from bash.

Shell programming can be accomplished by directly executing shell commands at the shell prompt or by storing them 
in the order of execution, in a text file, called a shell script, and then executing the shell script. To execute, 
simply write the shell script file name, once the file has execute permission (chmod +x filename).

The first line of the shell script file begins with a "sha-bang" (#!) which is not read as a comment, 
followed by the full path where the shell interpreter is located. This path, tells the operating system that this file 
is a set of commands to be fed into the interpreter indicated. Note that if the path given at the "sha-bang" is incorrect, 
then an error message e.g. "Command not found.", may be the result of the script execution. 
It is common to name the shell script with the ".sh" extension. The first line may look like this:

#!/bin/bash

Adding comments: any text following the "#" is considered a comment

To find out what is currently active shell, and what is its path, type the highlighted command at the shell prompt 
(sample responses follow):

ps | grep $$

987 tty1 00:00:00 bash

This response shows that the shell you are using is of type 'bash'. next find out the full path of the shell interpreter

which bash

/bin/bash

This response shows the full execution path of the shell interpreter. Make sure that the "sha-bang" 
line at the beginning of your script, matches this same execution path.



#!/bin/bash
# Text to the right of a '#' is treated as a comment - below is the shell command
echo 'Goodbye, World!'

>>>
Goodbye, World!
>>>




<h2 id="01.001.">01.002. Variables</h2>


Shell variables are created once they are assigned a value. A variable can contain a number, 
a character or a string of characters. Variable name is case sensitive and can consist of a combination of letters 
and the underscore "_". Value assignment is done using the "=" sign. 
Note that no space permitted on either side of = sign when initializing variables.




PRICE_PER_APPLE=5
MyFirstLetters=ABC
greeting='Hello        world!'


>>>

>>>



Referencing the variables
A backslash "\" is used to escape special character meaning


MyFirstLetters=ABC
echo "The first 10 letters in the alphabet are: ${MyFirstLetters}DEFGHIJ"


>>>
The first 10 letters in the alphabet are: ABCDEFGHIJ
>>>



Encapsulating the variable name with "" will preserve any white space values


greeting='Hello        world!'
echo $greeting" now with spaces: $greeting"


>>>
Hello world! now with spaces: Hello        world!
>>>




date -d "$date1" +%A


>>>

</body>
</html>
Tuesday
>>>



