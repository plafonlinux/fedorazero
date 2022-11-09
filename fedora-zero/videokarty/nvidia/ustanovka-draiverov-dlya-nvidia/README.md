# Установка драйверов для Nvidia

{% hint style="info" %}
В Fedora Linux 35 репозиторий с драйверами Nvidia теперь включается по дефолту, если при первичной настройке системы поставить галочку на активацию репозитория со стороннего репозитория.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/cVVJheR1328.jpg" alt=""><figcaption></figcaption></figure>

### Установка через Терминал:

```bash
sudo dnf install gcc kernel-headers kernel-devel akmod-nvidia xorg-x11-drv-nvidia xorg-x11-drv-nvidia-libs xorg-x11-drv-nvidia-power nvidia-settings 
```

```bash
sudo reboot
```
