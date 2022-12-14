---
description: Утилита для бекапа вашей системы
---

# Timeshift

Timeshift - это утилита работающая в двух режимах: RSYNC для создания полноценных снимков вашего диска и BTRFS где задействуется особенность файловой системы btrfs и появляется возможность создавать точки восстановления.

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-11-09 15-07-01.png" alt=""><figcaption></figcaption></figure>

## Установка

```bash
sudo dnf install timeshift
```

{% hint style="warning" %}
Для того чтобы работал корректно режим Btrfs необходимо [перенастроить Btrfs subvolumes](https://plafon.gitbook.io/fedora-zero/fedora-zero/bekap/nastraivaem-btrfs-subvolumes), так как утилита Timeshift создавалась под deb-подобные дистрибутивы и поэтому не понимает маркировку subvolumes в Fedora Linux.
{% endhint %}

{% hint style="success" %}
**Интересный факт:** Утилита Timeshift долгое время никак не "развивалась", да и вся "разработка" держалась на плечах одного лишь энтузиаста, который в итоге полностью отказался от дальнейшего развития своей программы. Поэтому разработку Timeshift подхватил проект Linux Mint и сделал его штатным придожением для бэкапа.
{% endhint %}
