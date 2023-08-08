---
description: Стандартным и идеальным браузером в Линуксе является Mozilla Firefox
---

# Браузеры



<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-08-06 08-39-33.png" alt=""><figcaption></figcaption></figure>

```bash
sudo dnf install firefox
```

### Дополнительные возможности:

В адресной строке вбиваем `about:config` и соглашаемся с рисками:

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2023-08-08 06-54-41.png" alt=""><figcaption></figcaption></figure>

* Включаем WebRender в Firefox

`gfx.webrender.all` ставим на `true`&#x20;

`widget.wayland-dmabuf-vaapi` ставим на `true`&#x20;

`widget.wayland-dmabuf-vaapi.enabled` ставим на `true`

* Включаем кинетический скролл:

`apz.gtk.kinetic_scroll.enabled` ставим на true Настраиваем скорость (по умолчанию 100)&#x20;

`mousewheel.default.delta_multiplier_` ставим на true&#x20;

`mousewheel.default.delta_multiplier_x` нужное число&#x20;

`mousewheel.default.delta_multiplier_y` нужное число&#x20;

`mousewheel.default.delta_multiplier_z` нужное число

### Но возможно тебе этого мало ....
