
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [py.processing](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/17/PROC.MD) - [Processing basics](https://github.com/ttltrk/ELSE/blob/master/PRF/CREATIVECODING.MD)

---

### Interactive

---

* [Write your own little drawing program]()
* [Enhance your little drawing program by adding mouse events!]()

---

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
