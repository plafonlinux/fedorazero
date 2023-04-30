---
description: Как примонтировать сетевые папки с NAS в Fedora Linux
---

# Сетевые папки (NAS)

<figure><img src="../../.gitbook/assets/dfdfdfdfdfdfd.png" alt=""><figcaption></figcaption></figure>

Я монтирую свои папки на Synology в fstab вот так:

```bash
sudo gnome-text-editor /etc/fstab
```

`//192.135.9.146/home/syno/Drive /mnt/Drive cifs uid=0,credentials=/home/username/.smb,iocharset=utf8,vers=3.0,noperm 0 0`

Предварительно создав директорию куда монтировать:

```bash
sudo mkdir Drive
```

и после сохранения файла fstab уже монтирую её

```bash
sudo systemctl daemon-reload
```

```bash
sudo mount -a
```

Ах ну и да, пароль и логин лежат в файле `/home/username/.smb`

`*username` имя пользователя в системе, чтобы увидеть файлы с .название, в nautilus нужно нажать сочетание клавиш `Ctrl+H`

Структура файла `.smb`:

```
user=имя_пользователя
password=пароль_учетки
domain=WORKGROUP
```
