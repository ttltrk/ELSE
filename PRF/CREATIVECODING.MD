
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [py.processing](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/17/PROC.MD)

---

### Processing basics (course document)

---

* [Introduction](https://github.com/ttltrk/ELSE/blob/master/PRF/01/INTRO.MD)
* [Setting things Up](https://github.com/ttltrk/ELSE/blob/master/PRF/02/SETTINGS.MD)
* [Starting to draw basic shapes](https://github.com/ttltrk/ELSE/blob/master/PRF/03/BASICSHAPES.MD)
* [It's Alive! Getting things moving]()
* [Interactive]()

  * <a href="#20">Write your own little drawing program</a>
  * <a href="#21">Enhance your little drawing program by adding mouse events!</a>

---

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
