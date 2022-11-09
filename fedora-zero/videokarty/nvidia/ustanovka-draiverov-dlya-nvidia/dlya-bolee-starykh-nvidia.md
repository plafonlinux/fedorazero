---
description: Установка драйверов для видеокарт Nvidia версий 340 и 390
---

# Для более "старых" Nvidia

{% hint style="info" %}
Не существует какого-то "упрощенного" метода для установки драйверов Nvidia версий 340 и 390. Таким образом была составлена данная инструкция!
{% endhint %}

{% hint style="danger" %}
**ПРЕДУПРЕЖДАЕМ!!! Wayland сессия не будет доступна**
{% endhint %}

{% hint style="warning" %}
Об 3D ускорении графики в таких проектах, как Wine, Proton и Bottles можно увы позабыть.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/3405_02.jpg" alt=""><figcaption></figcaption></figure>

## Подключаем репозиторий RPM Fusion

```bash
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
```

```bash
sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

## Установка 390 версии драйвера

{% hint style="info" %}
Для видеокарт GeForce 400/500 и частично 600 серии
{% endhint %}

```bash
sudo dnf install xorg-x11-drv-nvidia-390xx akmod-nvidia-390xx
```

{% hint style="success" %}
Перезагружаем ПК
{% endhint %}

## Установка 340 версии драйвера

{% hint style="info" %}
Для видеокарт GeForce 8/9/200/300 серий
{% endhint %}

```bash
sudo dnf install xorg-x11-drv-nvidia-340xx akmod-nvidia-340xx
```

{% hint style="success" %}
Перезагружаем ПК
{% endhint %}
