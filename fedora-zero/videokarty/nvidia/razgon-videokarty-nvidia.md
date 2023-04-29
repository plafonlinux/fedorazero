---
description: Включаем разгон Nvidia на Linux
---

# Разгон видеокарты NVIDIA

{% hint style="danger" %}
#### Всё в данном разделе вы делаете на свой страх и риск! Будьте внимательны!
{% endhint %}

```bash
sudo mkdir /etc/X11/xorg.conf.d/
```

```bash
sudo gnome-text-editor /etc/X11/xorg.conf.d/20-nvidia.conf
```

далее добавляем в файл:

```bash
Section "Device"
Identifier "Device0"
Driver "nvidia"
VendorName "NVIDIA Corporation"
BoardName "НАЗВАНИЕ ВАШЕЙ ВИДЕОКАРТЫ"

#если у вас уже есть настройки в файле, достаточно добавить два пункта ниже.

Option "RegistryDwords" "PerfLevelSrc=0x2222"
Option "TripleBuffer" "True"
Option "Coolbits" "28"
EndSection
Section "Screen"
Identifier "Screen0"
Device "Device0"
Monitor "Monitor0"
DefaultDepth 24
Option "Stereo" "0"
Option "nvidiaXineramaInfoOrder" "DFP-0"

#если у вас уже есть настройки в файле, достаточно добавить пункт ниже.

Option "metamodes" "nvidia-auto-select +0+0 { ForceFullCompositionPipeline = On }"
Option "SLI" "Off"
Option "MultiGPU" "Off"
Option "BaseMosaic" "off"
SubSection "Display"
Depth 24
EndSubSection
EndSection
```

{% hint style="warning" %}
```
Редактируем BoardName "НАЗВАНИЕ ВАШЕЙ ВИДЕОКАРТЫ"
```
{% endhint %}

{% hint style="success" %}
Сохраняем CTRL+O, ENTER, CTRL+X
{% endhint %}
