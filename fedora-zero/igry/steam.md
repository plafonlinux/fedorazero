---
description: Самая крутая игровая платформа для Линукса
---

# Steam

<figure><img src="../../.gitbook/assets/1634980031764 (1).jpg" alt=""><figcaption><p>Steam запущенный на GNU/Linux</p></figcaption></figure>

### Установка:

```bash
flatpak install flathub com.valvesoftware.Steam
```

### Включаем Proton (Steam Play) для запуска игр на линуксе

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 10-53-32.png" alt=""><figcaption><p>Steam Play включает Proton</p></figcaption></figure>

### Кэш шейдеров улучшает плавность игры

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 10-55-01.png" alt=""><figcaption></figcaption></figure>

### Дополнительные параметры запуска (ProtonDB) вставляются здесь:

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 10-56-36.png" alt=""><figcaption></figcaption></figure>

### Мой диск не видно в Steam из Flatpak

Добавляем путь до нашего `диска/каталога` в утилите `Flatseal`

```bash
flatpak install flathub com.github.tchx84.Flatseal
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 10-59-55.png" alt="flatseal steam flatpak"><figcaption><p>Добавляем нужный каталог в Steam Flatpak через утилиту Flatseal</p></figcaption></figure>

Например у меня это диск примонтированный как каталог `/games`&#x20;
