---
description: Если ты совсем рисковый, то можно пойти дальше ....
---

# Обновление до Beta

{% hint style="danger" %}
Вы делаете всё на свой страх и риск! Но любопытство оно такое ...
{% endhint %}

### Как обновиться уже сейчас с Fedora 37 (в будущем просто меняем на 38/39 и т.д.):

```bash
sudo dnf makecache --refresh && sudo dnf upagrade --refresh
```

```bash
sudo dnf autoremove && sudo dnf clean all
```

```bash
sudo dnf install dnf-plugin-system-upgrade -y
```

```bash
sudo dnf system-upgrade download --releasever=37
```

```bash
sudo dnf system-upgrade reboot
```

Если метод выше не работает или есть ошибки:

```bash
sudo dnf system-upgrade download --releasever=37 --allowerasing --skip-broken
```

```bash
sudo dnf system-upgrade reboot
```

```bash
sudo dnf system-upgrade clean
```

Если же и `--allowerasing` не работает, то пробуем:

```bash
sudo dnf distro-sync
```

```bash
sudo fixfiles -B onboot
```

{% hint style="info" %}
И пробуем снова.
{% endhint %}

{% hint style="danger" %}
ПОМНИТЕ! ВЫ ДЕЛАЕТЕ ВСЁ НА СВОЙ СТРАХ И РИСК!

НЕТ ОСТРОЙ НЕОБХОДИМОСТИ ОБНОВЛЯТЬСЯ C ВЕРСИИ НА ВЕРСИЮ, ЛУЧШЕ НАПРОТИВ ПОДОЖДАТЬ ДНЕЙ 10 С РЕЛИЗА И УЖЕ ПОТОМ ОБНОВИТЬСЯ ШТАТНО ЧЕРЕЗ GNOME SOFTWARE.
{% endhint %}
