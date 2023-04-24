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

### Если Flatpak Telegram не использует установленную тему для курсора мыши

```bash
flatpak --user override --filesystem=/home/$USER/.icons/:ro org.telegram.desktop
```

```bash
flatpak --user override --filesystem=/usr/share/icons/:ro org.telegram.desktop
```

### Включаем системную рамку на Wayland

Переводим Telegram на XWayland в утилите Flatseal

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-11-05 13-04-33 (1) (2).png" alt=""><figcaption></figcaption></figure>

Включаем рамку в настройках Telegram

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-11-05 13-04-56.png" alt=""><figcaption></figcaption></figure>
