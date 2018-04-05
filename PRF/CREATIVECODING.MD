
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [py.processing](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/17/PROC.MD)

---

### Processing basics (course document)

---

* [Introduction](https://github.com/ttltrk/ELSE/blob/master/PRF/01/INTRO.MD)
* [Setting things Up]()

  * <a href="#3">Recent chnages on processing.org</a>
  * <a href="#4">Download and Insstall on Mac</a>
  * <a href="#5">Download and Insstall on Win</a>
  * <a href="#6">Discover the processing user interface</a>


* [Starting to draw basic shapes]()

  * <a href="#7">Prepare your drawing board</a>
  * <a href="#8">Use the different basic shapes</a>
  * <a href="#9">One additional shape and greyscales</a>

* [It's Alive! Getting things moving]()

  * <a href="#10">Improve the setup and act random</a>
  * <a href="#11">Exercise: random size</a>
  * <a href="#12">Exercise: random size solution</a>
  * <a href="#13">Create moving laser beams</a>
  * <a href="#14">More fun with lines</a>

* [Interactive]()

  * <a href="#20">Write your own little drawing program</a>
  * <a href="#21">Enhance your little drawing program by adding mouse events!</a>

---

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

### <h3 id="7">Prepare your drawing board</h3>

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

Use a ```Comment```

```
size(600,400);
//the next line will create an ellipse
ellipse(100, 150, 50, 50);
rectMode(CENTER);
rect(100, 150, 50, 50);
```

Changing the order of the shapes

```
size(600,400);
//the next line will create an ellipse
rect(100, 150, 50, 50);
ellipse(100, 150, 50, 50);
```

### <h3 id="9">One additional shape and greyscales</h3>

Triangle

```
size(800,600);
triangle(50,50,  700,200,  300,500);
```

Another traingle

```
size(800,600);
triangle(50,50,  700,200,  300,500);
triangle(-100,400,  500,200,  600,1000);
```

stroke() //grey border was set

```
size(800,600);
triangle(50,50,  700,200,  300,500);
stroke(150);
triangle(-100,400,  500,200,  600,1000);
```

the triangle border was changed

```
size(800,600);
strokeWeight(10);
triangle(50,50,  700,200,  300,500);
stroke(150);
triangle(-100,400,  500,200,  600,1000);
```

the first border was removed

```
size(800,600);
strokeWeight(10);
noStroke();
triangle(50,50,  700,200,  300,500);

stroke(150);
strokeWeight(10);
triangle(-100,400,  500,200,  600,1000);
```

fill()

```
size(800,600);
strokeWeight(10);
noStroke();
triangle(50,50,  700,200,  300,500);

stroke(150);
strokeWeight(10);
fill(50);
triangle(-100,400,  500,200,  600,1000);
```

It's Alive! Getting things moving
------

### <h3 id="10">Improve the setup and act random</h3>

Using random()

```
void setup() {
  size(500,500);
  background(random(256));
  ellipse(width/2, height/2, 100,100);
}
```

### <h3 id="13">Create moving laser beams</h3>
 
 using draw()
 
 ```
 void setup() {
  size(500,500); 
}

void draw() {
  background(random(256));
  ellipse(width/2, height/2, 100,100);
}
```

frameRate() will change the blinking to 2 sec

```
void setup() {
  size(500,500); 
  frameRate(2);
}

void draw() {
  background(random(256));
  ellipse(width/2, height/2, 100,100);
}
```

making a line

```
void setup() {
  size(500,500); 
  frameRate(2);
  background(0);
}

void draw() {
  stroke(255,0,0);
  line(0,0,  width, height);
}
```

changing the line size, with random (numbers) command

```
void setup() {
  size(500,500); 
  frameRate(2);
  background(0);
}

void draw() {
  stroke(random(255),0,0);
  line(0,0,  width, height);
}
```

use the random cmd for the line (angle) too

```
void setup() {
  size(500,500); 
  //frameRate(2);
  background(0);
}

void draw() {
  stroke(random(255),0,0);
  line(0,0,  random(width), random(height));
}
```

central

```
void setup() {
  size(500,500); 
  //frameRate(2);
  background(0);
}

void draw() {
  stroke(random(255),0,0);
  line(width/2,height/2,  random(width), random(height));
}
```

with green lines

```
void setup() {
  size(500,500); 
  //frameRate(2);
  background(0);
}

void draw() {
  stroke(0, random(255),0);
  line(width/2,height/2,  random(width), random(height));
}
```

### <h3 id='14'>More fun with lines</h3>

creaitng black lines

```
void setup() {
  size(600,600); 
  background(255);
  stroke(0);
}

void draw() {
  line(0,random(height),  width,random(height));
}
```

```
void setup() {
  size(600,600); 
  background(255);
  frameRate(1);
  stroke(0);
}

void draw() {
  background(255);
  float yPosition = random(height);
  line(0,yPosition,  width,yPosition);
}
```

Section 5 - Interactive
------

### <h3 id="20">Write your own little drawing program</h3>

drawing with mouse

```
void setup() {
  size(800, 800);
  background(255);
}

void draw() {
  ellipse(mouseX, mouseY, 40, 40);
}
```

### <h3 id="21">Enhance your little drawing program by adding mouse events!</h3>

[[]()]

You can better draw with mouse click

```
boolean painting = false;

void setup() {
  size(800, 800);
  background(255);
}

void draw() {
  
  if(painting == true) {
    ellipse(mouseX, mouseY, 40, 40);  
  }
}

void mouseClicked() {
  
  painting =! painting;
  println(painting);
  
}
```

---

* [src - Coding for beginners: learn coding by creating art](https://www.udemy.com/creativecoding/learn/v4/content)
* [src - processing.org](https://processing.org/)

---
