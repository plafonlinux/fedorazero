---
description: KDE Connect для GNOME
---

# GS Connect (KDE Connect)

Устанавливаем: `GSConnect`

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 13-30-00.png" alt=""><figcaption></figcaption></figure>

### Настраиваем Firewall

```bash
sudo firewall-cmd --zone=public --permanent --add-port=1714-1764/tcp
```

```bash
sudo firewall-cmd --zone=public --permanent --add-port=1714-1764/udp
```

```bash
sudo systemctl restart firewalld.service
```

### OpenSSL:

```bash
sudo dnf install openssl
```

Скачиваем приложение для смартфона и конектимся (работает только в одной WiFi сети):

{% embed url="https://f-droid.org/packages/org.kde.kdeconnect_tp/" %}

{% hint style="warning" %}
Обязательно перезапускаем ПК/ноутбук
{% endhint %}
