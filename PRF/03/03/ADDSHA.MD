
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [basic manuals](https://github.com/ttltrk/PRG/blob/master/MANUALS.MD) - [Scripts](https://github.com/ttltrk/PRG/blob/master/PY/DOC/SC/SC.MD) - [Python](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/OPYM.MD) - [py.processing](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/17/PROC.MD) - [Processing basics](https://github.com/ttltrk/ELSE/blob/master/PRF/CREATIVECODING.MD) - [Basic shapes](https://github.com/ttltrk/ELSE/blob/master/PRF/03/BASICSHAPES.MD)

---

### One additional shape and greyscales

---

* [Triangle](https://github.com/ttltrk/ELSE/blob/master/PRF/03/03/01/TRI.MD)
* [Another traingle](https://github.com/ttltrk/ELSE/blob/master/PRF/03/03/02/TTRI.MD)
* [stroke() //grey border was set]()
* [the triangle border was changed]()
* [the first border was removed]()
* [fill()]()

---

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

---
