# Меняем версию ядра

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-31 10-47-34.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
В Fedora Linux после обновлений системы, всегда доступны 3 версии ядра, на случай если у вас что-то не будет на самом свежем, всегда можно откатиться на предыдущее, где всё работало.
{% endhint %}

Устанавливаем утилиту `grubby`

```bash
sudo dnf install grubby
```

Смотрим список доступных ядер в системе:

```bash
sudo grubby --info=ALL | grep -E "^kernel|^index"
```

Получаем что-то похожее на это:

```bash
index=0
kernel="/boot/vmlinuz-6.0.5-200.fc36.x86_64"
index=1
kernel="/boot/vmlinuz-5.19.16-301.fc37.x86_64"
index=2
kernel="/boot/vmlinuz-5.19.16-200.fc36.x86_64"
index=3
kernel="/boot/vmlinuz-0-rescue-e5e0486de0354ed5adbd9418f209953e"
```

Выбираем версию ядря, которую хотим использовать (выбрав нужный `index` из списка)

```bash
sudo grubby --set-default-index=0
```

В примере выше я выбрал `kernel 6.0` у которого `index=0`

Проверям всё ли применилось:

```bash
sudo grubby --default-title
```

<figure><img src="../../.gitbook/assets/Снимок экрана от 2022-10-31 10-56-28.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Перезагружаем ПК
{% endhint %}
