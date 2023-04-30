---
description: Для обладателей твердотельных накопителей SSD.
---

# Fstab

{% hint style="warning" %}
Помимо стандартных параметров монтирования я через запятую добавляю ещё эти 3 после **`compress=zstd:1`**
{% endhint %}

Открываем `fstab` командой в терминале (CTRL+ALT+T):

```bash
sudo gnome-text-editor /etc/fstab
```

и добавляем данные параметры после **`compress=zstd:1`**

```
,defaults,noatime,discard=async
```

Для разделов: `/, /home, /var/log`

<figure><img src="../../.gitbook/assets/UdCWLp1UYNc (1).jpg" alt="fstab edit fedora zero linux"><figcaption><p>Редактирование Fstab в GNU/Linux</p></figcaption></figure>
