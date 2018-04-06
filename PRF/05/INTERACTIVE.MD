
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
