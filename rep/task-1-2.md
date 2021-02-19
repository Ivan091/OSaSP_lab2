(2) Выполнить все задания пункта 1, создавая не жёсткие, а символьные ссылки

Изучаем назначение и ключи команды ln

```bash
man ln
```

Создаем файл

```bash
nano 1-2_file.txt
```

Пишем текст

```
The storm broke today
and the sun came out.
```

Сохраняем нажатием: `Ctrl` + `X`, `Y`, `Enter`.

Создаём символьную ссылку на файл

```bash
ln -s 1-2_file.txt 1-2_file-link.txt
```

Просматриваем содержимое файла с помощью сслыки

```bash
cat 1-2_file-link.txt
```

```
The storm broke today
and the sun came out.
```

Удаляем файл

```bash
rm 1-2_file.txt
```

Просматриваем содержимое файла с помощью сслыки

```bash
cat 1-2_file-link.txt
```

```
cat: 1-2_file-link.txt: No such file or directory
```

Создаем каталог

```bash
mkdir 1-2_katalog
```

Создаем жёсткую ссылку на каталог

```bash
ln -s 1-2_katalog 1-2_katalog-link
```
