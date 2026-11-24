# HModeling Tools

[Русский](#русский) · [English](#english)

| Houdini | Platform | Download |
| --- | --- | --- |
| 22.0.466 | Windows x64 | [SOP_HModelingTools.dll](22.0.466/dso/SOP_HModelingTools.dll) |
| 22.0.466 | Linux x86-64 | [SOP_HModelingTools.so](22.0.466/dso/SOP_HModelingTools.so) |
| 22.0.466 | macOS arm64 | [SOP_HModelingTools.dylib](22.0.466/dso/SOP_HModelingTools.dylib) |
| 22.0.429 | Windows x64 | [SOP_HModelingTools.dll](22.0.429/dso/SOP_HModelingTools.dll) |
| 22.0.368 | Windows x64 | [SOP_HModelingTools.dll](22.0.368/dso/SOP_HModelingTools.dll) |
| 22.0.368 | Linux x86-64 | [SOP_HModelingTools.so](22.0.368/dso/SOP_HModelingTools.so) |
| 22.0.368 | macOS arm64 | [SOP_HModelingTools.dylib](22.0.368/dso/SOP_HModelingTools.dylib) |

## Русский

### Установка

1. Скачайте файл для точной версии Houdini и своей платформы.
2. Закройте Houdini и скопируйте файл в `$HOUDINI_USER_PREF_DIR/dso/`. Создайте папку `dso`, если её ещё нет. На Windows стандартный путь — `Documents/houdini22.0/dso/` в профиле пользователя.
3. Запустите Houdini. Ноды доступны в SOP-меню **Tab → HModeling Tools**.

Если две сборки Houdini используют одну папку настроек, меняйте плагин при смене сборки. Для Linux нужны glibc 2.38+ и libstdc++ с `GLIBCXX_3.4.32`. [Контрольные суммы](SHA256SUMS.txt)

Сборки macOS предназначены для Apple Silicon (arm64). В бинарниках указана минимальная версия macOS 27.2.

### Последние изменения · Windows x64 · 22.0.466, 22.0.429, 22.0.368

- **Edit Poly · Выделение.** `Shift` добавляет соседний полигон и поверх манипулятора. Быстрые клики по разным граням обрабатываются отдельно. Двойная ЦКМ выбирает кольцо рёбер и в режимах Move, Rotate и Scale.

## English

### Installation

1. Download the file for your exact Houdini build and platform.
2. Close Houdini and copy the file into `$HOUDINI_USER_PREF_DIR/dso/`. Create the `dso` folder if needed. On Windows, the default is `Documents/houdini22.0/dso/` in your user profile.
3. Start Houdini. Find the SOP nodes under **Tab → HModeling Tools**.

If two Houdini builds share one preferences folder, swap the plugin when switching builds. Linux requires glibc 2.38+ and libstdc++ providing `GLIBCXX_3.4.32`. [Checksums](SHA256SUMS.txt)

The macOS builds target Apple Silicon (arm64). The binaries specify macOS 27.2 as their minimum deployment version.

### Latest changes · Windows x64 · 22.0.466, 22.0.429, 22.0.368

- **Edit Poly · Selection.** Shift-click adds a neighboring polygon even over the transform handle. Fast clicks on different faces are handled separately. Double middle-click selects an edge ring in Move, Rotate, and Scale.
