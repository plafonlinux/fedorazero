---
description: Установка Wine на Fedora Linux
---

# Wine HQ

### **Что такое Wine HQ?**

Wine - набор инструментов помогающих "воссоздать" необходимую среду для запуска приложений/игр созданных конкретно под платформу на Windows.

На основе Wine, был создан и дополнен разработчиками Valve, аналог под название Proton, что значительно улучшило качество запускаемых игр.

Оригинальный Wine заточен на запуск любого Windows совместимого приложения, но 100% работающий экземепляр ожидать не стоит.

<figure><img src="../../.gitbook/assets/wine-hq.webp" alt="wine hq fedora linux"><figcaption><p>Wine is not an emulator</p></figcaption></figure>

```bash
sudo dnf config-manager --add-repo https://dl.winehq.org/wine-builds/fedora/32/winehq.rep
```

```bash
sudo dnf install winehq-devel
```

```bash
wget https://raw.githubusercontent.com/Winetricks/winetricks/master/src/winetricksas
```

```bash
chmod +x winetricks
```

```bash
sudo mv -v winetricks /usr/bin/
```