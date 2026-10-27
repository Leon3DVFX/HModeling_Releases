# HModeling Tools

[Русский](#русский) · [English](#english)

| Houdini | Platform | Plugin |
| --- | --- | --- |
| **22.0.429** | Windows x64 | [SOP_HModelingTools.dll](22.0.429/dso/SOP_HModelingTools.dll) |
| **22.0.368** | Windows x64 | [SOP_HModelingTools.dll](22.0.368/dso/SOP_HModelingTools.dll) |

## Русский

Набор инструментов моделирования и UV для Houdini:

- **Edit Poly** — полигональное моделирование, инструменты кривых, Soft Selection и история операций.
- **UV Editor** — отдельное окно UV с выделением, синхронизированным с 3D-вьюпортом.
- **Marmoset Bridge** — передача геометрии в Toolbag для рендера.

Обе сборки — **22.0.429** и **22.0.368** — включают поддержку Global UI Scale для панелей и справки,
выделение петель через A+MMB в T/R/E и исправления ошибок справки и обновления
панелей.

Ускорены интерактивные трансформации и подсветка предпросмотра, в том числе при временном сглаживании во вьюпорте.

### Установка

1. Выберите папку, совпадающую с **полной версией Houdini**, включая номер сборки. Пакеты проверены на **22.0.368** и **22.0.429, Windows x64**.
2. Закройте Houdini. Скопируйте содержимое `<версия>/dso/` в `<HOUDINI_USER_PREF_DIR>/dso/`. В стандартной установке Windows это папка `Documents/houdini22.0/dso/` в профиле пользователя. Создайте `dso`, если её ещё нет; при переопределённой папке настроек используйте свой путь.
3. Запустите Houdini. Ноды доступны в SOP-меню **Tab → HModeling Tools**.

Разные сборки Houdini могут использовать общую папку настроек. При переходе между ними
заменяйте DLL на соответствующую полной версии Houdini: несовпадение сборок может вызвать падение.

Справка RU/EN и иконки встроены в DLL. Откройте справку кнопкой **? / Help** нужной ноды. Для Marmoset Bridge укажите путь к установленному Toolbag.
Разделитель между оглавлением и страницей справки можно перетаскивать, меняя ширину областей.

Пакет имеет статус **Alpha**. Режим Baker в Marmoset Bridge пока не реализован. Совместимость с другими сборками Houdini и другими ОС не заявлена.

Контрольная сумма DLL находится в [SHA256SUMS.txt](SHA256SUMS.txt). Лицензия — [MIT](LICENSE).

## English

Modeling and UV tools for Houdini:

- **Edit Poly** — polygon modeling, curve tools, Soft Selection and operation history.
- **UV Editor** — a separate UV window with selection synchronized with the 3D viewport.
- **Marmoset Bridge** — geometry transfer to Toolbag for rendering.

Both **22.0.429** and **22.0.368** builds include Global UI Scale support for panels and Help,
A+MMB loop selection in T/R/E, and Help and panel refresh fixes.

Interactive transforms and preview highlighting are faster, including while viewport subdivision is enabled.

### Installation

1. Choose the folder matching the **full Houdini version**, including its build number. Packages are tested on **22.0.368** and **22.0.429, Windows x64**.
2. Close Houdini. Copy the contents of `<version>/dso/` into `<HOUDINI_USER_PREF_DIR>/dso/`. On a standard Windows installation this is `Documents/houdini22.0/dso/` in your user profile. Create `dso` if needed; use your configured location if the preferences folder has been overridden.
3. Start Houdini. Find the SOP nodes under **Tab → HModeling Tools**.

Different Houdini builds may share the same preferences folder. When switching builds,
replace the DLL with the one matching the full Houdini version: a mismatched DLL may crash Houdini.

RU/EN help and icons are embedded in the DLL. Open a node's reference with its **? / Help** button. For Marmoset Bridge, set the path to your installed Toolbag executable.
Drag the divider between the Help contents and page to adjust their widths.

This package is **Alpha**. Marmoset Bridge's Baker mode is not implemented yet. Compatibility with other Houdini builds or operating systems is not claimed.

The DLL checksum is listed in [SHA256SUMS.txt](SHA256SUMS.txt). License: [MIT](LICENSE).
