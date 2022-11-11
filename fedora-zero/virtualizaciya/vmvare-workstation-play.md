# VMVare Workstation Play

## Скачиваем VMVare Workstation

<figure><img src="../../.gitbook/assets/tn-work-station-player.png" alt="VMVare Workstation Player Fedora Workstation Gnome"><figcaption><p>VMVare Workstation Player</p></figcaption></figure>

{% embed url="https://www.vmware.com/go/getplayer-linux" %}

Установка VMWare&#x20;

```bash
sudo bash ./VMware-Player-Full-16.2.4-20089737.x86_64.bundle --eulas-agreed --required
```

```bash
sudo vmware-modconfig --console --install-all
```

Установка linux-headers

```bash
sudo dnf install kernel-devel
```

Установка модулей (для ядра 6.0 и выше)

```bash
wget https://github.com/mkubecek/vmware-host-modules/archive/player-16.2.4.tar.gz
```

```bash
tar -xzf player-16.2.4.tar.gz
```

```bash
cd vmware-host-modules-player-16.2.4/
```

```bash
sudo make && sudo make install
```

```bash
mv vmmon-only vmmon
```

```bash
mv vmnet-only vmnet
```

```bash
sudo cp -a vmmon vmnet /usr/lib/vmware/modules/source/
```

```bash
sudo vmware-modconfig —console —install-all
```

Перезапускаем сервис:

```bash
systemctl restart vmware.service
```

Проверяем статус сервиса:

```bash
systemctl status vmware.service
```

{% hint style="info" %}
Запускаем Vmware и закрываем.
{% endhint %}

Включаем 3D-ускорение:

```bash
sudo nano ~/.vmware/preferences 
```

надо добавить строчку

```bash
mks.gl.allowBlacklistedDrivers = "TRUE"
```

{% hint style="success" %}
Всё, VMware теперь полностью готов к работе! Спасибо нашему подписчику в VK
{% endhint %}
