(1) Изучить назначение и ключи команды ln.
- создать жесткую ссылку на файл. Просмотреть содержимое файла, используя ссылку. Удалить файл. Просмотреть содержимое файла. Объяснить результат;
- создать жесткую ссылку на каталог. Объяснить результат;

Изучаем назначение и ключи команды ln

```bash
man ln
```

Создаем файл

```bash
nano 1-1_file.txt
```

Пишем текст

```
The storm broke today
and yhe sun came out.
```

Сохраняем нажатием: `Ctrl` + `X`, `Y`, `Enter`.

Создаём жёсткую ссылку на файл

```bash
ln 1-1_file.txt 1-1_file-link.txt
```

Просматриваем содержимое файла с помощью сслыки

```bash
cat 1-1_file-link.txt
```

```
The storm broke today
and yhe sun came out.
```

Удаляем файл

```bash
rm 1-1_file.txt
```

Просматриваем содержимое файла с помощью сслыки

```bash
cat 1-1_file-link.txt
```

```
The storm broke today
and the sun came out.
```

Создаем каталог

```bash
mkdir 1-1_katalog
```

Создаем жёсткую ссылку на каталог

```bash
ln 1-1_katalog 1-1_katalog-link
```

```
ln: 1-1_katalog: hard link not allowed for directory
```
