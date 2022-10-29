---
description: Ручная разметка в дистрибутиве Fedora Linux
---

# Разметка диска

{% hint style="warning" %}
Всем пользователям, настоятельно рекомендуется использовать автоматическую разметку в установщике Fedorа Linux (Anaconda).
{% endhint %}

{% hint style="danger" %}
Будьте внимательны! Автоматическая установка полностью "затирает" диск куда будет устанавливаться система!
{% endhint %}

### Как установить Fedora в дуалбуте с Windows?

{% embed url="https://www.youtube.com/watch?v=VaIgbTOvAd0" %}

### Ручная разметка Fedora Linux

{% embed url="https://www.youtube.com/watch?v=DIp4yqIe8O4" %}

### Для того чтобы заработал Timeshift

{% hint style="info" %}
Чтобы всё заработало правильно, необходимо настроить правильно при ручной разметке в Blivet-GUI subvolumes для btrfs (порядок создания снизу-вверх!)
{% endhint %}

<figure><img src="../../.gitbook/assets/VctyhmmHO-Y.jpg" alt=""><figcaption></figcaption></figure>

```
@log /var/log
@home /home
@ /
```
