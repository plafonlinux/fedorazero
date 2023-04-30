---
description: Шпаргалка как управлять GitHub на Linux
---

# GitHub

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-04-30 16-06-56.png" alt=""><figcaption></figcaption></figure>

Для того чтобы залогиниться в свой аккаунт на **GitHub**, теперь достаточно использовать утилиту `gh` и следовать указаниям (логинимся в браузере). Если ввести в терминале `gh`, то будет предложено установить данную утилиту, либо устанавливаем её сами:

```bash
sudo dnf install gh -y
```

01\. Выбираем куда скачать репозиторий:

```bash
cd ~/Документы
```

02\. Далее клонируем его: (на примере `plafonlinux/swayconfig`):

<figure><img src="../../.gitbook/assets/Снимок экрана от 2023-04-30 16-18-12.png" alt=""><figcaption></figcaption></figure>

```bash
git clone https://github.com/plafonlinux/swayconfig.git
```

или силами утилиты `gh`

```
gh repo clone plafonlinux/swayconfig
```

```bash
cd swayconfig
```

```bash
git pull
```

```bash
git add .
```

```bash
git commit -s "Описание ваших изменений"
```

```bash
git push
```
