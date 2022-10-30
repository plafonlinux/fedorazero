---
description: Делаем красивый терминал на ZSH
---

# Терминал на ZSH

{% hint style="success" %}
Большая благодарность автору канала [`Toxblh. Не только Linux`](https://t.me/toxblh\_linux) за предоставленный гайд и сорсы.
{% endhint %}

{% embed url="https://github.com/Toxblh/dotfiles" %}

### Качаем архив с конфигами и шрифтами:&#x20;

{% file src="../../.gitbook/assets/Terminal_Fedora_PLAFON.zip" %}

### Закидываем .zshrc в папку /home

<figure><img src="../../.gitbook/assets/Vu6xVEHHTGc.jpg" alt=""><figcaption></figcaption></figure>

### Устанавливаем ZSH в Fedora Linux

```bash
sudo dnf install zsh
```

### Делаем ZSH по умолчанию для нашего терминала:

```bash
grep tecmint /etc/passwd
```

```bash
chsh -s $(which zsh)
```

```bash
grep tecmint /etc/passwd
```

{% hint style="info" %}
Перезапускаем ПК
{% endhint %}

```bash
zsh
```
