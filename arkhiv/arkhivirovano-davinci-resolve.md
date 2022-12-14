# \[Архивировано] DaVinci Resolve

<figure><img src="../.gitbook/assets/uOxMCNPt3TI.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
## МЕТОД УСТАРЕЛ ИЛИ БЫЛ УПРОЩЕН! ДАННАЯ СТРАНИЦА АРХИВИРОВАНА
{% endhint %}

## Подготовка системы

Устанавливаем проприетарный OpenCL в Fedora

```bash
git clone https://github.com/sukhmeetbawa/OpenCL-AMD-Fedora.git
```

```bash
cd ./OpenCL-AMD-Fedora
```

```bash
./opencl-amd.sh
```

{% hint style="success" %}
Выбираем _**lastest**_ и жмём _**Ввод**_
{% endhint %}

Проверяем всё ли работает утилитой `clinfo`

```bash
sudo dnf install clinfo
```

```bash
clinfo
```

Далее устанавливаем недостающую либу: `mesa-libGLU`

```bash
sudo dnf install mesa-libGLU
```

{% hint style="success" %}
Перезапускаем ПК
{% endhint %}

## Теперь качаем и устанавливаем сам DaVinci Resolve

<figure><img src="../.gitbook/assets/Снимок экрана от 2022-10-30 18-20-53.png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.blackmagicdesign.com/products/davinciresolve" %}

{% embed url="https://www.youtube.com/watch?v=39_wWFBcP2E" %}

