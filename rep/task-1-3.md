(3) Создать жесткую и символьную ссылки на файл. С помощью команды ls
просмотреть inod файла и ссылок. Объяснить результат.

---

Создаём файл

```bash
nano 1-3_file.txt
```

---

Пишем текст

```
The storm broke today
and the sun came out.
```

---

Сохраняем нажатием: `Ctrl` + `X`, `Y`, `Enter`.

---

Просматриваю inod

```bash
ls -i
```

```
2628857 1-3_file.txt
```

---

Создаём жёсткую ссылку на файл.

```bash
ln 1-3_file.txt 1-3_file-link-1.txt
```

---

Просматриваю inod

```bash
ls -i
```

```
2628857 1-3_file-link-1.txt
2628857 1-3_file.txt
```

---

Создаём символьную ссылку на файл.

```bash
ln -s 1-3_file.txt 1-3_file-link-2.txt
```

---

Просматриваю inod

```bash
ls -i
```

```
2628857 1-3_file-link-1.txt
2628860 1-3_file-link-2.txt
2628857 1-3_file.txt
```
