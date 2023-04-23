---
description: Только для X.org
---

# Убираем тиринг на AMD

{% hint style="info" %}
Тиринг, если в двух словах это “разрыв” картинки, который очень часто встречается на Линуксе. Все дело в устаревшей технологии дисплейного менеджера X.Org, который в ближайшие годы будет заменен полностью, на современную реализацию Wayland.
{% endhint %}

<figure><img src="../../../.gitbook/assets/Tearing-dello-schermo-o-input-lag.jpg" alt=""><figcaption><p>Пример тиринга</p></figcaption></figure>

```bash
sudo vim /etc/X11/xorg.conf.d/20-amdgpu.conf
```

и вставляем:

```bash
Section "Device"
Identifier "AMD"
Driver "amdgpu"
Option "TearFree" "true"
Option "DRI" "3"
EndSection
```

{% hint style="success" %}
Далее CTRL+O, ENTER, CTRL+X
{% endhint %}

### Тест на тиринг

{% embed url="https://www.youtube.com/watch?v=5xkNy9gfKOg" %}
