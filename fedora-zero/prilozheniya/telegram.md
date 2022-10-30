---
description: Мессенджер
---

# Telegram

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 11-41-28.png" alt="telegram fedora linux flathub flatpak"><figcaption><p>Telegram для Fedora Linux</p></figcaption></figure>

```bash
flatpak install flathub org.telegram.desktop
```

### Во Flatpak версии курсор больше, чем системный

```bash
sudo flatpak override --env=XCURSOR_SIZE=12 org.telegram.desktop
```
