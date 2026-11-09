# Логотипы IT Club Irkutsk

Варианты логотипа сообщества. База: **«IT Club Irkutsk»**, палитра максимум 3 цвета.

## Палитра (снята с logo-4-ice.png)

| Цвет | Hex | Назначение |
| ------ | --------- | ------------------------------- |
| Navy | `#013058` | фон неба/льда, тёмный круг |
| Teal | `#3CABB4` | вода, акценты |
| White | `#FDFDFD` | ледяные трещины, горы, текст |

Дополнительно в logo-5: `#0C2A52` (диск), `#1FB5A7` (бирюза-2), `#25B4BF` (текст Irkutsk) — в пределах лимита 3 цвета.

## Файлы

| Файл | Описание | Статус |
| -------------------- | -------------------------------------------------- | ----------------- |
| `logo-1-nerpa.png` | нерпа в проруби + пикселный `</>` в небе | старый, оставлен |
| `logo-2-mark.png` | чёрная монограмма IT: волна Ангары → контакт чипа | старый, оставлен |
| `logo-3-sketch.png` | не сохранился | генерация упала, не перезапускалась |
| `logo-4-ice.png` | лёд/горы/вода + IT CLUB IRKUTSK | фаворит (осн. эмблема) |
| `logo-5-mark.png` | диск с волнами + горизонтальный воркмарк | вторая лин. |
| `logo-4-ice.svg` | векторная перерисовка фаворита | вручную |

## Параметры генерации

Все растровые варианты: модель `opencode/gpt-image-2.5-sunburst`, 1254x1254, PNG (src RGBA).

### logo-1-nerpa.png (2026-11-09)

```
Circular flat vector logo for a tech community "IT CLUB IRKUTSK".
Baikal lake theme: minimalist Baikal seal (nerpa) silhouette floating
on stylized frozen waves with white ice cracks, above it small
pixel-like code brackets </> in the sky. Deep blue and teal flat
palette on white background, crisp geometric shapes, no gradients.
Bold sans-serif text "IT CLUB" and smaller "IRKUTSK" stacked inside
the circle. Single centered badge, clean edges, Telegram avatar
friendly.
```

Правки: `</>` удалён из неба (re-edit → current file), фон прозрачный (RGBA).

### logo-2-mark.png (2026-11-09)

```
Minimal square wordmark logo for "IRK IT CLUB" tech community.
Abstract monogram combining the letters IT with Angara river water
line and a circuit-trace node beneath, black ink on white, monoline
flat vector style, no gradients, no circle frame, small caption
"IRKUTSK" under the mark.
```

Проблема: модель добавила текст `"IRK IT CLUB"` + дублирующий `"IRKUTSK"` —
название получилось не по брендингу; печатная наработка знака рабочая.

### logo-3-sketch.png (2026-11-09)

```
Playful hand-drawn circular sticker "IT CLUB IRKUTSK": smiling
microchip character with legs and antennae on a wave, rough black
brush-pen lines, yellow accent, sketchy dots around circle edge.
```

Ошибка: генерация упала, файл не создан (сеть: timeout/connection drop).

### logo-4-ice.png (2026-11-09) — фаворит

```
Flat circular badge logo for tech community "IT CLUB IRKUTSK":
frozen lake with geometric white ice-crack lines, below the horizon
stylized teal wave bands, mountain ridge silhouette. Strictly 3 colors:
dark navy blue, teal, and white on transparent background. No gradients,
crisp flat vector shapes. Bold white bold sans-serif "IT CLUB" large and
"IRKUTSK" smaller beneath, inside the lower part of the deep navy circle
band. Single centered round emblem, clean edges, Telegram avatar friendly.
```

Правки: `</>` удалён (re-edit → current file); фон переведён из чёрного
в прозрачный (python/PIL flood-fill, ~667K px).

### logo-5-mark.png (2026-11-09)

```
Minimal flat vector logo, two colors (dark navy + teal) on white.
Round deep-navy disc with abstract geometric symbol: three horizontal
teal wave lines above a white underwater coil/circuit shape (Baikal +
electricity), no animals, no letters inside the disc. Wordmark
"IT Club" (navy bold) + "Irkutsk" (teal) beside/below. Square, lots
of white space, no gradients.
```

## Правила, учтённые в наборе

1. без животных (нерпа — исключение, «старый» вариант оставлен)
2. палитра max 3 цвета: navy + teal + white
3. базовое название: «IT Club Irkutsk»

## Планы

- ч/б и инвертированная версии фаворита (для печати/тёмного фона)
- SVG logo-5 тех же цветов, при необходимости — re-draw
