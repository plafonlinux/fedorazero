# MangoHUD

### Включаем мониторинг игр MangoHud в Steam Flatpak



```bash
flatpak install org.freedesktop.Platform.VulkanLayer.MangoHud
```

Включить для всех игр разом:

```bash
flatpak override --user --env=MANGOHUD=1 com.valvesoftware.Steam
```

Отключить для всех игр разом:

```bash
flatpak override --user --env=MANGOHUD=0 com.valvesoftware.Steam
```

Включить отдельно для каждой игры в Steam (Vulkan + OpenGL):

```bash
mangohud %command%
```

Включить отдельно для каждой игры в Steam (только Vulkan):

```bash
MANGOHUD=1
```
