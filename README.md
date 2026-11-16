# HModeling Tools

[Русский](#русский) · [English](#english)

| Houdini | Platform | Download |
| --- | --- | --- |
| 22.0.466 | Linux x86-64 | [SOP_HModelingTools.so](22.0.466/dso/SOP_HModelingTools.so) |
| 22.0.429 | Windows x64 | [SOP_HModelingTools.dll](22.0.429/dso/SOP_HModelingTools.dll) |
| 22.0.368 | Windows x64 | [SOP_HModelingTools.dll](22.0.368/dso/SOP_HModelingTools.dll) |
| 22.0.368 | Linux x86-64 | [SOP_HModelingTools.so](22.0.368/dso/SOP_HModelingTools.so) |

## Русский

### Установка

1. Скачайте файл для точной версии Houdini и своей платформы.
2. Закройте Houdini и скопируйте файл в `$HOUDINI_USER_PREF_DIR/dso/`. Создайте папку `dso`, если её ещё нет. На Windows стандартный путь — `Documents/houdini22.0/dso/` в профиле пользователя.
3. Запустите Houdini. Ноды доступны в SOP-меню **Tab → HModeling Tools**.

Если две сборки Houdini используют одну папку настроек, меняйте плагин при смене сборки. Для Linux нужны glibc 2.38+ и libstdc++ с `GLIBCXX_3.4.32`. [Контрольные суммы](SHA256SUMS.txt)

### Последние изменения · Windows x64 · 22.0.429 и 22.0.368

- **Refboard** по умолчанию выключен. Видимость запоминается для каждой ноды Edit Poly, раскладки общие для HIP. Картинки переиспользуются при переключении между нодами.
- Вход в Edit Poly ускорен. **Last Action** учитывает видимость и размер осей вьюпорта.

Сборки Linux в таблице относятся к предыдущему выпуску.

## English

### Installation

1. Download the file for your exact Houdini build and platform.
2. Close Houdini and copy the file into `$HOUDINI_USER_PREF_DIR/dso/`. Create the `dso` folder if needed. On Windows, the default is `Documents/houdini22.0/dso/` in your user profile.
3. Start Houdini. Find the SOP nodes under **Tab → HModeling Tools**.

If two Houdini builds share one preferences folder, swap the plugin when switching builds. Linux requires glibc 2.38+ and libstdc++ providing `GLIBCXX_3.4.32`. [Checksums](SHA256SUMS.txt)

### Latest changes · Windows x64 · 22.0.429 and 22.0.368

- **Refboard** starts off. Visibility is remembered for each Edit Poly node, and layouts are shared in the HIP. Images are reused across node switches.
- Edit Poly opens faster. **Last Action** adjusts to the viewport gnomon's visibility and size.

The Linux builds in the table are from the previous release.
