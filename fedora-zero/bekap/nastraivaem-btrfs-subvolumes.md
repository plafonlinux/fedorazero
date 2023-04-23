---
description: Перенос subvolume btrfs
---

# Настраиваем BTRFS subvolumes

Монтируем файловую систему

{% hint style="success" %}
Первым делом проверяем чтобы в вашей системе не было ничего примонтировано в директории `/mnt`
{% endhint %}

```bash
ls -a /mnt
```

<figure><img src="../../.gitbook/assets/2222222.png" alt=""><figcaption></figcaption></figure>

Если в директории уже что-то примонтировано, то просто нужно создать новую директорию и монтировать в нее.&#x20;

Например:

```bash
sudo mkdir /mnt/btrfs
```

{% hint style="warning" %}
В этом руководстве все команды будут выполнены с учетом того, что была создана директория `btrfs`
{% endhint %}

Дальше нужно определить на какое устройство установлена система:

```bash
df -h
```

<figure><img src="../../.gitbook/assets/333333.png" alt=""><figcaption></figcaption></figure>

Теперь монтируем файловую систему (c учетом ваших результатов):

```bash
sudo mount /dev/sda3 /mnt/btrfs
```

{% hint style="info" %}
Если открыть примонтированую директорию через файловый менеджер, то будут видны примонтированные подразделы (subvolume).
{% endhint %}

<figure><img src="../../.gitbook/assets/444444444444.png" alt=""><figcaption></figcaption></figure>

## Перенос подразделов

Теперь приступаем к переносу подразделов:

```bash
sudo mv /mnt/btrfs/root /mnt/btrfs/@
```

```bash
sudo mv /mnt/btrfs/home /mnt/btrfs/@home
```

<figure><img src="../../.gitbook/assets/5555555.png" alt=""><figcaption></figcaption></figure>

## Затем правим `fstab`:

```bash
sudo vim /etc/fstab
```

{% hint style="success" %}
Меняем root нa @ , а /home на @home
{% endhint %}

<figure><img src="../../.gitbook/assets/6666666666.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Сохраняем Ctrl+O , выходим Ctrl+X
{% endhint %}

Обновляем GRUB (обязательно!)

```bash
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
```

<figure><img src="../../.gitbook/assets/777777777777777.png" alt=""><figcaption></figcaption></figure>

## Размонтируем файловую систему

Сбросим все данные с хэша в файловую систему:

```bash
sync
```

Размонтируем файловую систему:

```bash
sudo umount -r /mnt/btrfs
```

{% hint style="success" %}
Теперь можно перезагрузить ПК
{% endhint %}

Командой `sudo btrfs sub list /` можно посмотреть какие подразделы у нас в данный момент.

<figure><img src="../../.gitbook/assets/999999999999.png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
ТЕПЕРЬ, КСТАТИ, БУДЕТ ПОЛНОЦЕННО РАБОТАТЬ TIMESHIFT
{% endhint %}
