---
description: Гибридная графика на Fedora Linux
---

# Установка драйверов для NVIDIA Optimus

{% hint style="info" %}
чиная с Fedora 31 и версии проприетарного драйвера 435.xx, технология NVIDIA Optimus, используемая в ноутбуках с гибридной графикой, поддерживается в полной мере «из коробки». К сожалению, старые поколения видеокарт (ниже серии 700) им не поддерживаются и поэтому работать не будут.
{% endhint %}

Подключим репозитории RPM Fusion:

```bash
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

Установим стандартный драйвер NVIDIA для современных видеокарт:

```bash
sudo dnf install gcc kernel-headers kernel-devel akmod-nvidia xorg-x11-drv-nvidia xorg-x11-drv-nvidia-libs
```

Если используется 64-битная ОС, но требуется запускать ещё и Steam и 32-битные версии игр, то установим также 32-битный драйвер (устанавливать сразу после предыдущих):

```bash
sudo dnf install xorg-x11-drv-nvidia-libs.i686
```

### **Действия по окончании установки:**

По окончании установки необходимо убедиться, что модули ядра были успешно собраны и установлены корректно:

```bash
sudo akmods --force
```

{% hint style="warning" %}
Если возникла ошибка, то подробный журнал можно найти в каталоге `/var/cache/akmods/nvidia/`
{% endhint %}

Теперь вырежем из образа [initrd](https://ru.wikipedia.org/wiki/Initrd) драйвер nouveau и добавим NVIDIA:

```bash
sudo dracut --force
```

### При возникновении чёрного экрана:

{% hint style="warning" %}
Если по окончании установки и перезагрузки вместо окна входа в систему нас встретит чёрный экран, то в загрузчике добавим через пробел следующие параметры ядра:
{% endhint %}

```bash
rd.drivers.blacklist=nouveau nouveau.modeset=0
```

{% hint style="info" %}
Также нужно в обязательном порядке зайти в модуль настройки UEFI компьютера или ноутбука и отключить [UEFI Secure Boot](https://ru.wikipedia.org/wiki/Secure\_boot) (сама Fedora поддерживает работу с Secure Boot, однако модули ядра проприетарного драйвера не имеют цифровой подписи, поэтому не могут быть загружены в данном режиме и, как следствие, пользователь увидит чёрный экран), а также перевести его из режима **Windows Only** в **Other OS**.
{% endhint %}

## Работа с NVIDIA Optimus

По умолчанию будет использоваться интегрированное решение, но для запуска приложения с использованием дискретной видеокарты необходимо передавать особые переменные окружения:

```bash
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia application [параметры запуска приложения]
```

Пример запуска <mark style="color:green;">**панели управления**</mark> <mark style="color:green;">**NVIDIA**</mark> для <mark style="color:green;">**Optimus**</mark> конфигураций:

```bash
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia nvidia-settings -c :8
```

Пример запуска приложения app.exe через Wine на Optimus:

```bash
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia wine app.exe
```

### **Удаление драйверов**

Если возникли какие-то проблемы, либо драйверы NVIDIA более не требуются, то их всегда можно удалить штатным способом:

```bash
sudo dnf remove \*nvidia\*
```

{% hint style="warning" %}
По окончании удаления необходимо в обязательном порядке пересобрать образ initrd, чтобы вернуть в него удалённый при установке свободный драйвер nouveau
{% endhint %}

```bash
sudo dracut --force
```

<details>

<summary>Источник</summary>

[https://www.easycoding.org/2017/01/11/pravilnaya-ustanovka-drajverov-nvidia-v-fedora.html](https://www.easycoding.org/2017/01/11/pravilnaya-ustanovka-drajverov-nvidia-v-fedora.html)

</details>
