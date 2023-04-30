---
description: Как подключить Xbox контроллер в Линуксе
---

# Xbox контроллер

<figure><img src="../../.gitbook/assets/1634980031764 (1).jpg" alt=""><figcaption></figcaption></figure>

### - Драйвер для этого _Wireless донгла_, называется **xone**

{% embed url="https://github.com/medusalix/xone" %}

**Установка:**

```bash
git clone https://github.com/medusalix/xone
```

```bash
cd xone
```

```bash
sudo dnf install dkms
```

```bash
sudo ./install.sh --release
```

```bash
cd install && sudo sh firmware.sh
```

{% hint style="success" %}
Перезапускаем ПК и должно всё заработать, геймпад законектится и перестанет мигать! 😎👌
{% endhint %}
