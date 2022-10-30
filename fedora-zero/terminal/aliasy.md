---
description: Alias
---

# Алиасы

## Добавляем Alias (сокращенные команды)

<figure><img src="../../.gitbook/assets/w7goacm-lkA.jpg" alt=""><figcaption></figcaption></figure>

```bash
    #
    # Timeshift
    #
    alias tm="sudo timeshift"
    alias tmc="sudo timeshift --create"
    alias tmd="sudo timeshift --delete"
    alias tmda="sudo timeshift --delete-all"
    alias tml="sudo timeshift --list"
    #
    # Neofetch
    #
    alias n="neofetch"
    alias k="uname -rs"
    alias g="gnome-shell --version"
    alias f="lsb_release -sd"
    alias m="inxi -G |grep Mesa"
    alias age="stat / | grep "Birth""
    #
    # DNF
    #
    alias up="sudo dnf makecache --refresh && sudo dnf upgrade --refresh -y && flatpak update -y"
    alias clean="sudo dnf autoremove -y && dnf clean all && flatpak uninstall --unused -y && sudo journalctl --vacuum-time=2weeks"
    #
    # PC
    #
    alias son="sudo systemctl suspend"
    alias logout="loginctl terminate-user ИМЯ_ВАШЕГО_ПОЛЬЗОВАТЕЛЯ"
    alias ls="ls --color"
    alias l="lsd --date '+%d.%m.%Y %H:%M' -lah"
    #
```
