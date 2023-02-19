---
description: Дробное масштабирование в GNOME
---

# Включаем дробное масштабирование

<figure><img src="../../.gitbook/assets/fedora_35_fractional_scaling.jpg" alt=""><figcaption></figcaption></figure>

```bash
gsettings set org.gnome.mutter experimental-features “[‘scale-monitor-framebuffer’]”
```

{% hint style="info" %}
Но включение дробного масштабирования, может привести к "мыльной" картинке, поэтому лично я увeличиваю "коэффициент масштабирования" самого текста в [Gnome Tweaks](https://plafon.gitbook.io/fedora-zero/fedora-zero/v-samom-nachale-.../dop.-nastroiki-gnome).
{% endhint %}

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-02-19 18-57-03.png" alt=""><figcaption></figcaption></figure>
