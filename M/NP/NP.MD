
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [M](https://github.com/ttltrk/ELSE/blob/master/M/M.MD) - [Tools](https://github.com/ttltrk/ELSE/blob/master/M/TOOLS/TOOLS.MD)

---

### Notepad ++

---

add char before after

```
before

Search: ^ 
Replace: <your_request>

after
Search: $ 
Replace: <your_request>
```

---

remove duplicates

```
Edit > Line Operations > Sort Lines Lexicographically Ascending 

Search: ^(.+?)\R(\1\R?)+
Replace: \1\r\n
```

---

all data in one line

```
Search: (\h*\R)+ 
Replace: \x20
```

---
