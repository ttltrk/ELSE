
[Coding for beginners: learn coding by creating art](https://www.udemy.com/creativecoding/learn/v4/content)
======

[performance.org](https://processing.org/)

### Introduction
  * <a href="#1">What this course is about</a>
  * <a href="#2">Why should you learn creative coding?</a>

### Setting things Up
  * <a href="#3">Recent chnages on processing.org</a>
  * <a href="#4">Download and Insstall on Mac</a>
  * <a href="#5">Download and Insstall on Win</a>
  * <a href="#6">Discover the processing user interface</a>

### Starting to draw basic shapes
  * <a href="#7">Prepare your draving board</a>
  * <a href="#8">Use the different basic shapes</a>

### Section

### Section

### Section

Introduction
------

### <h3 id="1">What this course is about</h3>

### <h3 id="2">Why should you learn creative coding?</h3>

Setting things Up
------

### <h3 id="3">Recent chnages on processing.org</h3>

### <h3 id="4">Download and Insstall on Mac</h3>

### <h3 id="5">Download and Insstall on Win</h3>

### <h3 id="6">Discover the processing user interface</h3>

Starting to draw basic shapes
------

### <h3 id="7">Prepare your draving board</h3>

Create bigger drawing board

```
size(500,500);
```

in the ```reference``` topic you can find more details about the commands

### <h3 id="8">Use the different basic shapes</h3>

Created one small point

```
size(600,400);
point(100,250);
```

Made a short line

```
size(600,400);
point(100,250);
point(101,250);
point(102,250);
point(103,250);
point(104,250);
point(105,250);
```

Made a longer line

```
size(600,400);
point(100,250);
point(101,250);
point(102,250);
point(103,250);
point(104,250);
point(105,250);
line(50, 50, 400, 200);
```

Create an ```ellipse```

```
size(600,400);
ellipse(100, 150, 50, 50);
```

Updated with ```rect```

```
size(600,400);
ellipse(100, 150, 50, 50);
rect(100, 150, 50, 50);
```

Covering the ```ellipse```

```
size(600,400);
ellipse(100, 150, 50, 50);
rectMode(CENTER);
rect(100, 150, 50, 50);
```

comment

```
size(600,400);
//the next line will create an ellipse
ellipse(100, 150, 50, 50);
rectMode(CENTER);
rect(100, 150, 50, 50);
```
