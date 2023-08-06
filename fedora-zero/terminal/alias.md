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
    alias age="stat / | grep Создан:
    c"
    alias ram="sudo dmidecode -t memory | grep Speed"
    alias cpu="lscpu | grep Имя"
    alias cpuc="lscpu"
    alias w="wine --version"
    alias pc="inxi -Ixxx"
    alias net="inxi -Nxxx"
    #
    # DNF
    #
    alias up="sudo dnf upgrade --refresh --best --allowerasing -y && flatpak update -y"
    alias cc="sudo dnf autoremove && dnf clean all && flatpak uninstall --unused -y && flatpak remove --delete-data && sudo journalctl --vacuum-time=1weeks"
    alias c="clear"
    alias dnfr="sudo dnf autoremove"
    alias dnfs="dnf search"
    alias dnfi="sudo dnf install"
    #
    # PC
    #
    alias son="sudo systemctl suspend"
    alias logout="loginctl terminate-user plafon"
    alias plafon="up && clean && clear && n"
    alias ls="ls --color"
    alias l="lsd --date '+%d.%m.%Y %H:%M' -lah"
    #
    # Flatpak
    #
    alias fli="flatpak install --noninteractive -y flathub"
    alias flr="flatpak remove --noninteractive -y"
    alias fr="flatpak repair"
    alias fl="flatpak list"
    #
    # Gnome Text Editor
    #
    alias gte="gnome-text-editor"
    alias sgte="sudo gnome-text-editor"
    #
    # System folders
    #
    alias fstab="sudo vim /etc/fstab"
    alias zshrc="vim .zshrc"
    alias bashrc="vim .bashrc"
    alias grubedit="sudo vim /etc/default/grub"
    alias upgrub="sudo grub2-mkconfig -o /boot/grub2/grub.cfg"
    #
    #
    #
    # DaVinci Resolve
    #
    alias convertmp4="find . -name '*.[mM][pP]4' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias convertmkv="find . -name '*.[mM][kK][vV]' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias convertmov="find . -name '*.[mM][oO][vV]' -execdir ffmpeg -i '{}' -c:v mpeg4 -qscale:v 1 -c:a pcm_s32le {}-davinci.mov \;"
    alias davinciconvdir="mkdir davinci;find . -name '*davinci.mov' -execdir mv {} ./davinci/ \;|cd davinci;rm -rf *'davinci.mov-davinci.mov'"
    alias convertall="convertmp4 && convertmkv && convertmov && davinciconvdir"
    #alias deletesource="ls | rm -rf *.mp4 && *.mov && *.mkv"
    alias convert="convertmp4 && convertmkv && convertmov && && davinciconvdir"
    #
    #
    #
    alias fstab="sudo vim /etc/fstab"
    alias zshrc="vim .zshrc"
    alias grubed="sudo vim /etc/default/grub"
    alias grubup="sudo grub2-mkconfig -o /boot/grub2/grub.cfg"
    alias cdvar="cd ~/.var/"
    alias cdconf="cd ~/.config/"
    alias cdssd="cd /mnt/davincissd"
    alias sn="sudo nautilus"
    #
    #
    #
    alias vmax="sudo sysctl -w vm.max_map_count=2147483642"
    alias vmax_check="sysctl -a | grep vm.max"#
```

