(1) Изучите при помощи man опцию -l команды ls. Просмотрите права каталогов `/etc`, `/bin` и `домашнего каталога`. Просмотрите права файлов, содержащиеся в этих каталогов. Выявите тенденции (файлов с какими правами в каких каталогах больше). Сделайте вывод.

---

Изучаем при помощи man опцию -l команды ls.

```bash
man ls
```

```
    -l     use a long listing format
```

---

Просматриваем права каталога `/etc`

```bash
ls -ld /etc
```

```
drwxr-xr-x 141 root root 12288 лют 19 01:02 /etc
```

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|d|rwx|r-x|r-x|
|директория|все права|доступ на чтение|доступ на чтение|

---

Просматриваем права каталога `/bin`

```bash
ls -ld /bin
```

```
lrwxrwxrwx 1 root root 7 лют 18 21:08 /bin -> usr/bin
```

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|l|rwx|rwx|rwx|
|символическая ссылка|все права|все права|все права|

---

Просматриваем права каталога `/home`

```bash
ls -ld /home
```

```
drwxr-xr-x 5 root root 4096 лют 18 21:42 /home
```

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|d|rwx|r-x|r-x|
|директория|все права|доступ на чтение|доступ на чтение|

---

Просмотр прав в каталоге `/etc`

```bash
ls -l /etc
```

Больше прав `drwxr-xr-x`

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|d|rwx|r-x|r-x|
|директория|все права|доступ на чтение|доступ на чтение|

---

Просмотр прав в каталоге `/bin`

```bash
ls -l /bin
```

```
lrwxrwxrwx 1 root root 7 лют 18 21:08 /bin -> usr/bin
```

```bash
ls -l /usr/bin
```

Больше прав `-rwxr-xr-x`

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|-|rwx|r-x|r-x|
|файл|все права|чтение и волнение|чтение и выполнение|

---

Просмотр прав в каталоге `/home`

```bash
ls -l /home
```

Больше прав `drwxr-xr-x`

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|d|rwx|r-x|r-x|
|директория|все права|доступ на чтение|доступ на чтение|
