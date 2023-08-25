---
description: Запускаем приложения/игры Windows через Wine/Proton
---

# PortProton

**PortProton** – это проект, разработанный для того, чтобы сделать легким и удобным запуск **Windows** игр на **Linux** как для начинающих, так и для продвинутых пользователей. Проект стремится сделать запуск игр (и другого программного обеспечения) максимально простым, но в то же время предоставляет гибкие настройки для продвинутых пользователей.

**PortProton** основан на версии WINE от Valve (Proton) и ее модификациях (Proton GE). Включает в себя набор скриптов в сочетании с самим WINE-PROTON, контейнером Steam Runtime Sniper с добавлением портированных версий MANGOHUD (вывод полезной информации через окно игры: FPS, FrameTime, CPU, GPU и т.д.) и vkBasalt (улучшение графики в играх, очень хорошо в сочетании с FSR, DLSS) + множество уже настроенных оптимизаций для максимальной производительности.

Реализована автоматическая установка в один клик (на вкладке АВТОУСТАНОВКА) популярных лаунчеров, таких как: **WGC, Epic Games, Battle.net , Origin, EVE Online, RockStar, Ubisoft connect, League of Legends** и многие другие.

{% embed url="https://linux-gaming.ru/2022/09/03/portproton/" %}

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-58-13 (1) (1).png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>

## Установка Port Proton на Fedora Linux

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-47-48.png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>

### Добавляем copr репозиторий:

```bash
sudo dnf copr enable boria138/portproton
```

### Устанавливаем сам PortProton:

```bash
sudo dnf update && sudo dnf upgrade --refresh && sudo dnf install portproton
```

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-58-13 (1) (1) (1) (1).png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-58-16 (1).png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-58-19.png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-11-09 07-58-21.png" alt="portproton proton wine windows fedora fedoralinux linux"><figcaption></figcaption></figure>
