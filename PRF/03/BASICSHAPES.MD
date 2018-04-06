
---

### Starting to draw basic shapes

---

* [Prepare your drawing board]()
* [Use the different basic shapes]()
* [One additional shape and greyscales]()

---

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

---
