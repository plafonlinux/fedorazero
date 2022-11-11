---
description: Кастомное мультимидийное ядро для игр
---

# Xanmod

<figure><img src="../../.gitbook/assets/xmk.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
УСТАНОВКА ЭТОГО ДОБРА НА СВОЙ СТРАХ И РИСК!
{% endhint %}

### Установка репозитория

```bash
sudo dnf copr enable rmnscnce/kernel-xanmod
```

### Установка ядра `edge` (подойдёт большинству)

Самое актуальное ядро

```bash
sudo dnf in kernel-xanmod-edge
```

LTS версия ядра

```bash
sudo dnf in kernel-xanmod-lts
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-11-11 15-07-48.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Перезапускаем ПК
{% endhint %}













## Другие варианты (для самых опытных)

{% hint style="danger" %}
ВЫ ТОЧНО ЗНАЕТЕ ЗАЧЕМ ВАМ ВСЁ ЭТО, ИБО ИНАЧЕ ЭТО ....&#x20;
{% endhint %}

`edge` собранный с LLVM+Clang и полным LTO

```bash
sudo dnf in kernel-xanmod-exptl
```

`edge` собранный с патчами TT-планировщика

```bash
sudo dnf in kernel-xanmod-tt
```

RT workloads

```bash
sudo dnf in kernel-xanmod-rt
```
