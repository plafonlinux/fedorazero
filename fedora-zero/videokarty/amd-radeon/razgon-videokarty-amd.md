---
description: Как включить разгон на AMD?!
---

# Разгон видеокарты AMD

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 13-41-07.png" alt=""><figcaption><p>CoreCTRL</p></figcaption></figure>

`amdgpu.ppfeaturemask=0xffffffff`

`radeon.cik_support=0 amdgpu.cik_support=1`

Параметры выше, нужно добавить через пробел в `/etc/default/grub`

```bash
sudo gnome-text-editor /etc/default/grub
```

Должно получится примерно так (_**кавычки важны!**_):

```bash
GRUB_CMDLINE_LINUX="ваши_параметры amdgpu.ppfeaturemask=0xffffffff radeon.cik_support=0 amdgpu.cik_support=1"
```

<figure><img src="../../../.gitbook/assets/coO6sAeE_0Y.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Далее CTRL+O, ENTER, CTRL+X
{% endhint %}

И пересобираем GRUB чтобы закрепить новые параметры, командой:

```bash
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
```
