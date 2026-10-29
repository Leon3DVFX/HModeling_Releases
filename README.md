# HModeling Tools

[Русский](#русский) · [English](#english)

| Houdini | Platform | Plugin |
| --- | --- | --- |
| **22.0.429** | Windows x64 | [SOP_HModelingTools.dll](22.0.429/dso/SOP_HModelingTools.dll) |
| **22.0.368** | Windows x64 | [SOP_HModelingTools.dll](22.0.368/dso/SOP_HModelingTools.dll) |
| **22.0.368** | Linux x86-64 | [SOP_HModelingTools.so](22.0.368/dso/SOP_HModelingTools.so) |

## Русский

Набор инструментов моделирования и UV для Houdini:

- **Edit Poly** — полигональное моделирование, инструменты кривых, Soft Selection и история операций.
- **UV Editor** — отдельное окно UV с выделением, синхронизированным с 3D-вьюпортом.
- **Marmoset Bridge** — передача геометрии в Toolbag для рендера.

Обе сборки — **22.0.429** и **22.0.368** — включают поддержку Global UI Scale для панелей и справки,
выделение петель через A+MMB в T/R/E и исправления ошибок справки и обновления
панелей.

Обновления предпросмотра трансформаций согласованы с кадрами вьюпорта; подготовленные данные подсветки используются повторно.

Текущие Windows-сборки добавляют отдельный **Slicer** в меню **Extra** всех компонентов
Edit Poly и применение прямого среза Cutter при отпускании ЛКМ. **Step Snap** задаёт
шаг трансформаций при удержании `J` в Edit Poly и UV Editor. Обновлены всплывающие
панели и справка RU/EN. Linux-пакет сохранён без изменений и пока не включает эти обновления.

В UV Editor `Q` возвращает режим Select, `T/R/E` включают трансформации, а `D` позволяет настроить рабочий пивот.
Снэп `S` поддерживает UV-точки, середины рёбер, центры полигонов и целые U/V. Свёрнутая панель Tools оставляет только стрелку.

### Установка

1. Выберите папку, совпадающую с **полной версией Houdini**, включая номер сборки, и файл своей платформы: `.dll` для Windows или `.so` для Linux. Windows x64 проверена на **22.0.368** и **22.0.429**. Linux-сборка **22.0.368** предоставлена и протестирована коллегой на **Debian 13, x86-64**.
2. Закройте Houdini. Скопируйте выбранный файл из `<версия>/dso/` в `<HOUDINI_USER_PREF_DIR>/dso/`. В стандартной установке Windows это папка `Documents/houdini22.0/dso/` в профиле пользователя. Создайте `dso`, если её ещё нет; при переопределённой папке настроек используйте свой путь.
3. Запустите Houdini. Ноды доступны в SOP-меню **Tab → HModeling Tools**.

Разные сборки Houdini могут использовать общую папку настроек. При переходе между ними
заменяйте плагин на соответствующий полной версии Houdini: несовпадение сборок может вызвать падение.

Для Linux требуются **glibc 2.38+** и **libstdc++ с `GLIBCXX_3.4.32`**.

Справка RU/EN и иконки встроены в плагин. Откройте справку кнопкой **? / Help** нужной ноды. Для Marmoset Bridge укажите путь к установленному Toolbag.
Разделитель между оглавлением и страницей справки можно перетаскивать, меняя ширину областей.

Пакет имеет статус **Alpha**. Режим Baker в Marmoset Bridge пока не реализован. Совместимость с другими сборками Houdini и окружениями не заявлена.

Контрольные суммы плагинов находятся в [SHA256SUMS.txt](SHA256SUMS.txt). Лицензия — [MIT](LICENSE).

## English

Modeling and UV tools for Houdini:

- **Edit Poly** — polygon modeling, curve tools, Soft Selection and operation history.
- **UV Editor** — a separate UV window with selection synchronized with the 3D viewport.
- **Marmoset Bridge** — geometry transfer to Toolbag for rendering.

Both **22.0.429** and **22.0.368** builds include Global UI Scale support for panels and Help,
A+MMB loop selection in T/R/E, and Help and panel refresh fixes.

Transform preview updates follow viewport frames; prepared highlighting data is reused.

The current Windows builds add a separate **Slicer** under **Extra** for every Edit Poly
component mode and apply Cutter's straight slice on LMB release. **Step Snap** uses
transform increments while holding `J` in Edit Poly and UV Editor. Popup panels and
RU/EN Help are updated. The Linux package is unchanged and does not yet include these updates.

In UV Editor, `Q` returns to Select, `T/R/E` activate transforms, and `D` edits the working pivot.
`S` snaps to UV points, edge midpoints, polygon centers and integer U/V. Collapsed Tools leave only an arrow.

### Installation

1. Choose the folder matching the **full Houdini version**, including its build number, and your platform's file: `.dll` for Windows or `.so` for Linux. Windows x64 is tested on **22.0.368** and **22.0.429**. The Linux **22.0.368** build was provided and tested by a colleague on **Debian 13, x86-64**.
2. Close Houdini. Copy the selected file from `<version>/dso/` into `<HOUDINI_USER_PREF_DIR>/dso/`. On a standard Windows installation this is `Documents/houdini22.0/dso/` in your user profile. Create `dso` if needed; use your configured location if the preferences folder has been overridden.
3. Start Houdini. Find the SOP nodes under **Tab → HModeling Tools**.

Different Houdini builds may share the same preferences folder. When switching builds,
replace the plugin with the one matching the full Houdini version: a mismatched build may crash Houdini.

Linux requires **glibc 2.38+** and **libstdc++ providing `GLIBCXX_3.4.32`**.

RU/EN help and icons are embedded in the plugin. Open a node's reference with its **? / Help** button. For Marmoset Bridge, set the path to your installed Toolbag executable.
Drag the divider between the Help contents and page to adjust their widths.

This package is **Alpha**. Marmoset Bridge's Baker mode is not implemented yet. Compatibility with other Houdini builds or environments is not claimed.

Plugin checksums are listed in [SHA256SUMS.txt](SHA256SUMS.txt). License: [MIT](LICENSE).
