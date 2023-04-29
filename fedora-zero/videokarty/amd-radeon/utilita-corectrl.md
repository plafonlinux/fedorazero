---
description: Утилита для управления AMD Radeon
---

# Утилита CoreCtrl

<figure><img src="../../../.gitbook/assets/Снимок экрана от 2022-10-29 13-41-07.png" alt=""><figcaption></figcaption></figure>

```bash
sudo dnf install corectrl
```

### Отключаем постоянные запросы пароля

```bash
sudo gnome-text-editor /etc/polkit-1/rules.d/90-corectrl.rules
```

и вставляем это:

```bash
polkit.addRule(function(action, subject) {
    if ((action.id == "org.corectrl.helper.init" ||
         action.id == "org.corectrl.helperkiller.init") &&
        subject.local == true &&
        subject.active == true &&
        subject.isInGroup("your-user-group")) {
            return polkit.Result.YES;
    }
});

```

Меняем `your-user-group` на имя пользователя в системе и сохраняем всё:

{% hint style="warning" %}
Перезагружаем ПК
{% endhint %}

### Настраиваем автозапуск CoreCtrl

<div>

<figure><img src="../../../.gitbook/assets/JkJ9ahcVwkw.jpg" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/ECoMiiBbFZc.jpg" alt=""><figcaption></figcaption></figure>

</div>
