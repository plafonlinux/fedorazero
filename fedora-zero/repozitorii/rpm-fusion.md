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

_Free_ repository

```bash
sudo dnf install \
  https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
```

_Nonfree_ repository

```bash
sudo dnf install \
  https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

United RPMs (опционально) | [Что это такое?](https://unitedrpms.github.io/)

```bash
sudo rpm --import https://raw.githubusercontent.com/UnitedRPMs/unitedrpms/master/URPMS-GPG-PUBLICKEY-Fedora
```

```bash
sudo dnf -y install https://github.com/UnitedRPMs/unitedrpms/releases/download/20/unitedrpms-$(rpm -E %fedora)-20.fc$(rpm -E %fedora).noarch.rpm
```

{% hint style="success" %}
Рекомендуется перезагрузить сессию, либо сам ПК.
{% endhint %}
