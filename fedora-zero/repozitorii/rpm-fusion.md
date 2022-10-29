---
description: Где весь софт в Fedora Linux?!
---

# RPM Fusion

{% hint style="info" %}
RPM Fusion – это репозиторий, распространяющий программное обеспечение, которое **Red Hat** и **Fedora Project** не хотят делать доступными в своих собственных репозиториях, в основном по лицензионным причинам, поскольку **Red Hat** предоставляет только программное обеспечение с открытым исходным кодом.
{% endhint %}

Все программное обеспечение, имеющееся в **RPM Fusion**, уже предварительно скомпилировано в формате **RPM**, просто нужно выполнить поиск в системном хранилище или ввести одну команду в терминале.

```bash
sudo dnf search НАЗВАНИЕ_ПАКЕТА
```

**RPM Fusion** был создан как комбинация из трех других репозиториев: _Dribble, Freshrpms и Livna_, с целью распространения как можно большего количества программного обеспечения в одном месте.

### Как включить RPM Fusion?

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-29 12-48-51.png" alt=""><figcaption></figcaption></figure>

```bash
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpms
```

После рекомендуется перезагрузить сессию, либо сам ПК.
