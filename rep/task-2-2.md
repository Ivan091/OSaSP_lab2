(2) Изучите материал, посвящѐнный пользователям и группам пользователей. Изучите руководство по командам `chown` и `chgrp`. Выясните, кто является владельцем и к какой группе владельцов принадлежат файлы вашего домашнего каталога, каталогов `/etc`, `/root`, `/bin` и `/dev`.

---

Изучаем руководство по команде `chown`

```bash
man chown
```

---

Изучаем руководство по команде `chgrp`

```bash
man chgrp
```

---

Выясняем владельца и групу владельца `домашнего каталога`

```bash
ls -ld ~
```

```
drwxr-xr-x 21 pavel-innokentevich-galanin pavel-innokentevich-galanin 4096 лют 20 02:01 /home/pavel-innokentevich-galanin
```

|Владелец|Группа владельца|
|-|-|
|pavel-innokentevich-galanin|pavel-innokentevich-galanin|

---

Выясняем владельца и групу владельца `/etc`

```bash
ls -ld /etc
```

```
drwxr-xr-x 141 root root 12288 лют 19 01:02 /etc
```

|Владелец|Группа владельца|
|-|-|
|root|root|

---

Выясняем владельца и групу владельца `/root`

```bash
ls -ld /root
```

```
drwx------ 8 root root 4096 лют 19 12:53 /root
```

|Владелец|Группа владельца|
|-|-|
|root|root|

---

Выясняем владельца и групу владельца `/bin`

```bash
ls -ld /bin
```

```
lrwxrwxrwx 1 root root 7 лют 18 21:08 /bin -> usr/bin
```

|Владелец|Группа владельца|
|-|-|
|root|root|

---

```bash
ls -ld /usr/bin
```

```
drwxr-xr-x 2 root root 69632 лют 19 00:28 /usr/bin
```

|Владелец|Группа владельца|
|-|-|
|root|root|

---

Выясняем владельца и групу владельца `/dev`

```bash
ls -ld /dev
```

```
drwxr-xr-x 21 root root 4820 лют 19 20:11 /dev
```

|Владелец|Группа владельца|
|-|-|
|root|root|
