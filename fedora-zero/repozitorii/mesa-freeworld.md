---
description: Драйверы vaapi и vdpau для GPU декодирования на AMD Radeon
---

# Mesa-freeworld

{% hint style="danger" %}
ТОЛЬКО ДЛЯ ОПЫТНЫХ ПОЛЬЗОВАТЕЛЕЙ ИЛИ ДЛЯ ТЕХ КТО ПОНИМАЕТ ЗАЧЕМ ЭТО НУЖНО!
{% endhint %}

{% hint style="info" %}
Команда проекта Fedora Linux [отключила декодирование](https://debugpointnews.com/fedora-37-mesa/) h264dec, h264enc, h265dec, h265enc и vc1dec через GPU, начиная с Fedora 37 и выше. Пакет Mesa, предоставляющий эту функцию, представил переключатель для отключения запатентованных кодеков. До сих пор по недосмотру он был включен в Fedora, что могло послужить поводом для нападков "патентных троллей".
{% endhint %}

{% hint style="info" %}
Таким образом команда [RPM Fusion](https://rpmfusion.org/) инициировала проверку, чтобы позволить пользователям самостоятельно включать пакет Mesa с включенными вышеперечисленными кодеками. Предлагаемое имя пакета `mesa-freeworld`.
{% endhint %}

{% hint style="success" %}
Драйверы Mesa vaapi и vdpau для кодирования/декодирования видео с ускорением на графическом процессоре (посредством видеокарты) теперь доступны (в тестовом порядке) в RPMFusion для Fedora 37 и Rawhide.
{% endhint %}

VAAPI

```bash
sudo dnf install --enablerepo=rpmfusion-free-updates-testing mesa-va-drivers-freeworld
```

VDPAU

```bash
sudo dnf install --enablerepo=rpmfusion-free-updates-testing mesa-vdpau-drivers-freeworld
```

Если уже установлены mesa-va-drivers или mesa-vdpau-drivers

```bash
sudo dnf swap --enablerepo=rpmfusion-free-updates-testing mesa-va-drivers mesa-va-drivers-freeworld
```

или

```bash
sudo dnf swap --enablerepo=rpmfusion-free-updates-testing mesa-vdpau-drivers mesa-vdpau-drivers-freeworld
```
