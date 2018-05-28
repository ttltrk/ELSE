

---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [M](https://github.com/ttltrk/ELSE/blob/master/M/M.MD) - [UX](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD)

---

### Cron

---

```
*      *    *          *     *
minute hour day(month) month day(week)

4 example:

At 00:05 in August.”
 at 2018-08-01 00:05:00

5 0 * 8 *
```

list all the jobs from cron between 22:00 and 23:00

```
crontab -l | grep "** 22"
```

edit cron

```
crontab -e
```

---

[src](https://crontab.guru/)

---
