(3) Определите атрибуты файлов `/etc/shadow` и `/etc/passwd` попробуйте вывести на экран содержимое этих файлов. Объясните результат.

---

Определяю атрибуты

```bash
ls -l /etc/shadow
```

```
-rw-r----- 1 root shadow 1388 лют 18 23:57 /etc/shadow
```

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|-|rw-|r--|---|
|файл|чтение и запись|чтение|нет прав|

---

Пробуем вывести файл

```bash
cat /etc/shadow
```

```
cat: /etc/shadow: Permission denied
```

---

Определяю атрибуты

```bash
ls -l /etc/passwd
```

```
-rw-r--r-- 1 root root 2652 лют 18 23:57 /etc/passwd
```

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|-|rw-|r--|r--|
|файл|чтение и запись|чтение|чтение|

---

Пробуем вывести файл

```bash
cat /etc/passwd
```

Файл вывелся в консоль
