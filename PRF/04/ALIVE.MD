
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [py.processing](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/17/PROC.MD) - [Processing basics](https://github.com/ttltrk/ELSE/blob/master/PRF/CREATIVECODING.MD)

---

### It's Alive! Getting things moving

---

* [Improve the setup and act random]()
* [Exercise: random size]()
* [Exercise: random size solution]()
* [Create moving laser beams]()
* [More fun with lines]()

---

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

---
