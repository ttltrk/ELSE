
---

### One additional shape and greyscales

---

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

---
