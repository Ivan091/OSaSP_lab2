(5) Выполните задание предыдущего пункта, используя в команде `chmod` только символы прав доступа.

---

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|файл|все права|нет прав|нет прав|
|-|rwx|---|---|
| |111|000|000|
| |7  |0  |0  |

```bash
touch file-1.txt

chmod a-rwx file-1.txt
chmod u+rwx file-1.txt
chmod g-rwx file-1.txt
chmod o-rwx file-1.txt

ls -l file-1.txt
```

```
-rwx------ 1 pavel-innokentevich-galanin pavel-innokentevich-galanin 0 лют 20 02:49 file-1.txt
```

---

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|файл|чтение и запись|чтение|все права|
|-|rw-|r--|rwx|
| |110|100|111|
| |6  |4  |7  |

```bash
touch file-2.txt

chmod a-rwx file-2.txt
chmod u+rw file-2.txt
chmod g+r file-2.txt
chmod o+rwx file-2.txt

ls -l file-2.txt
```

```
-rw-r--rwx 1 pavel-innokentevich-galanin pavel-innokentevich-galanin 0 лют 20 02:57 file-2.txt
```

---

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|файл|исполнение и запись|нет прав|чтение|
|-|-wx|---|r--|
| |011|000|100|
| |3  |0  |4  |

```bash
touch file-3.txt

chmod a-rwx file-3.txt
chmod u+wx file-3.txt
chmod g-rwx file-3.txt
chmod o+r file-3.txt

ls -l file-3.txt
```

```
--wx---r-- 1 pavel-innokentevich-galanin pavel-innokentevich-galanin 0 лют 20 03:00 file-3.txt
```

---

|-|Владелец|Группы|Остальные|
|-|---|---|---|
|файл|запись|все права|запись|
|-|-w-|rwx|-w-|
| |010|111|010|
| |2  |7  |2  |

```bash
touch file-4.txt

chmod a-rwx file-4.txt
chmod u+w file-4.txt
chmod g+rwx file-4.txt
chmod o+w file-4.txt

ls -l file-4.txt
```

```
--w-rwx-w- 1 pavel-innokentevich-galanin pavel-innokentevich-galanin 0 лют 20 03:02 file-4.txt
```
