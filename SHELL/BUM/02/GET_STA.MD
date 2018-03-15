
---

### Getting started

---

[<<<](https://github.com/ttltrk/ELSE/blob/master/SHELL/BUM/BUM.MD)

---

* <a href="#01">What is Unix</a>
* <a href="#02">Unix Architecture</a>
* <a href="#03">Login and Logout</a>
* <a href="#04">Password</a>
* <a href="#05">System Shutdown</a>

---

<h3 id="01">What is Unix</h4>

The Unix operating system is a set of programs that act as a 
link between the computer and the user.

The computer programs that allocate the system resources and coordinate all the details 
of the computer's internals is called the operating system or the kernel.

Users communicate with the kernel through a program known as the shell. 
The shell is a command line interpreter; it translates commands entered by the user and converts 
them into a language that is understood by the kernel.

---

<h3 id="02">Unix Architecture</h4>

```
Hardware --> Kernel --> Shell --> Application Programs
```

---

<h3 id="03">Login and Logout</h4>

Login

```
login:
pwd:
```

Logout

```
logout
```

---

<h3 id="04">Password</h4>

```
passwd
```

---

<h3 id="05">System Shutdown</h4>

|Command|Description|
|-------|-----------|
|halt|Brings the system down immediately|
|init 0|Powers off the system using predefined scripts to synchronize and clean up the system prior to shutting down|
|init 6|Reboots the system by shutting it down completely and then restarting it|
|poweroff|Shuts down the system by powering off|
|reboot|Reboots the system|
|shutdown|Shuts down the system|

---

[src](https://www.tutorialspoint.com/unix/unix-getting-started.htm)

---
