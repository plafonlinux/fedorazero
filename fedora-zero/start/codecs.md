---
description: Мультимедийные кодеки для Fedora Linux
---

# Установка кодеков

Не воспроизводиться видео? Установи кодеки!

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-11-05 18-57-49.png" alt=""><figcaption></figcaption></figure>

```bash
sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel
```

```bash
sudo dnf install lame\* --exclude=lame-devel
```

```bash
sudo dnf group upgrade --with-optional Multimedia
```
