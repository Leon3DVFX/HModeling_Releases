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

Обновления предпросмотра трансформаций, Extrude и Bevel согласованы с отрисовкой вьюпорта;
промежуточные изменения объединяются, а подготовленные данные подсветки используются повторно.
Фиолетовая заливка и живое сглаживание SubD сохранены.

Текущие Windows-сборки добавляют отдельный **Slicer** в меню **Extra** всех компонентов
Edit Poly и применение прямого среза Cutter при отпускании ЛКМ. **Step Snap** задаёт
шаг трансформаций при удержании `J` в Edit Poly и UV Editor. Обновлены всплывающие
панели и справка RU/EN. Уменьшено число лишних точек в срезах Cutter/Slicer; исправлена
видимость подсветки на обратной стороне полигонов. Slicer получил Smooth на основе NURBS,
режим Knife с Reverse side и Series с контролем расстояния во вьюпорте. Зажатое колесо
перемещает контур целиком, вращение колеса меняет число контуров. Linux-пакет сохранён
без изменений и пока не включает эти обновления.

В UV Editor `Q` возвращает режим Select, `T/R/E` включают трансформации, а `D` позволяет настроить рабочий пивот.
Снэп `S` поддерживает UV-точки, середины рёбер, центры полигонов и целые U/V. Свёрнутая панель Tools оставляет только стрелку.
`Alt` + перетаскивание ПКМ плавно меняет масштаб вокруг места нажатия, дополняя зум колесом.
Активные UDIM-тайлы обозначены тонкой янтарной рамкой и уголками, независимо от выделения UV.
Windows-сборки добавляют три чекера и загрузку изображения с диска для 2D и штатного 3D-отображения.
В нижней панели UV доступны диагностика формы и относительной площади для 2D и 3D; масштаб чекера независим от Texture Res.
Shape и Relative area автоматически отображаются в 2D и штатном 3D. Они тонируют включённый чекер или изображение, сохраняя рисунок; без картинки показывают самостоятельную цветовую заливку. Существующий флажок 3D управляет только текстурой. Штатный SubD сохраняется. Навигация с Alt сохраняет отображение; выход из State ноды, закрытие редактора или перепривязка восстанавливают прежние настройки viewport. Это временное отображение без изменения геометрии, Cd или материалов.
Изображения загружаются в фоне; предыдущая картинка той же ноды остаётся видимой до готовности новой. Загруженные изображения кэшируются без уменьшения разрешения и сжатия с потерями. Повторно откройте файл для обновления после внешнего изменения. Отсутствующий или неподдерживаемый файл вызывает явное сообщение об ошибке.
Direction оставляет только подписи ячеек. Repeat и Alpha управляют повтором и прозрачностью фона только в 2D.
Новые UV-инструменты Windows-сборок: **Orient U/V** поворачивает целый шелл по направлению выбранных компонентов,
а **Straighten Shell** выпрямляет открытую цепочку точек или рёбер к ближайшей U/V и расслабляет остальной шелл,
сохраняя Pin UV. Для Straighten сначала снимите Lock Area/Rotation. **Rectangle H/V** можно пробовать на любом
выбранном шелле; неподдерживаемая топология или конфликт ограничений отклоняет всю операцию с объяснением.
Граничные цепочки выделения останавливаются на углах и полюсах UV-топологии. Доступны Undo/Redo, повтор `G` и обновлённая справка RU/EN.
В сохранённом Linux-пакете этих UV-обновлений пока нет; для них нужна новая Linux-сборка.
Текущие Windows-сборки также добавляют **Insert Points** в основное радиальное меню сплайнов:
вставку, перемещение и удаление точек полилинии одной партией. Удаление сегментов разделяет сплайн.

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

Transform, Extrude and Bevel preview updates follow viewport drawing; intermediate changes
are coalesced and prepared highlighting data is reused. Violet fill and live SubD are retained.

The current Windows builds add a separate **Slicer** under **Extra** for every Edit Poly
component mode and apply Cutter's straight slice on LMB release. **Step Snap** uses
transform increments while holding `J` in Edit Poly and UV Editor. Popup panels and
RU/EN Help are updated. Cutter/Slicer cuts create fewer redundant points, and cut highlighting
remains visible on back-facing polygons. Slicer now includes NURBS-based Smooth, Knife with
Reverse side, and Series with a viewport spacing control. MMB drag moves the entire contour;
the wheel changes the contour count. The Linux package is unchanged and does not yet include
these updates.

In UV Editor, `Q` returns to Select, `T/R/E` activate transforms, and `D` edits the working pivot.
`S` snaps to UV points, edge midpoints, polygon centers and integer U/V. Collapsed Tools leave only an arrow.
`Alt` + RMB drag smoothly zooms around the press position, alongside wheel zoom.
Active UDIM tiles have a thin amber frame and corner marks, independently of UV selection.
The Windows builds add three checkers and disk image loading for 2D and native 3D display.
The bottom UV strip provides shape and relative-area diagnostics in 2D and 3D; checker scale is independent of Texture Res.
Shape and Relative area appear automatically in 2D and native 3D. They tint an enabled checker or image while preserving its pattern; without an image they show standalone colors. The existing 3D checkbox controls the texture only. Native SubD is preserved. Alt navigation keeps the display; leaving the node State, closing the editor or rebinding restores previous viewport preferences. This temporary display does not edit geometry, Cd or materials.
Images load in the background; the previous image for the same node remains visible until the new image is ready. Loaded images are cached without downsampling or lossy conversion. Open the file again to refresh it after an external edit. Unsupported or missing images report an explicit error.
Direction uses cell IDs only. Repeat and Alpha control tiling and opacity of the 2D background only.
New UV tools in the Windows builds: **Orient U/V** rotates whole shells using selected components as a direction reference.
**Straighten Shell** straightens an open point or edge chain to its nearest U/V axis and relaxes the surrounding shell,
keeping Pin UV exact; unlock shell area/rotation before Straighten. **Rectangle H/V** can be tried on any selected shell;
unsupported topology or conflicting constraints reject the complete operation with a reason.
Boundary selection chains stop at topological corners and poles. Native Undo/Redo, repeat `G` and updated RU/EN Help are included.
The retained Linux package does not yet include these UV additions and needs a new Linux build.
The current Windows builds also add **Insert Points** in the main spline marking menu:
insert, move and delete polyline points in one batch. Deleting spline segments splits the curve.

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
