# Squoosh
## 1. Аналіз вихідних файлів
### Виберіть 3 типи зображень (фотографія, скріншот, графічне зображення з текстом).
### Зафіксуйте їхній початковий розмір, формат (JPEG, PNG тощо) та вагу файлу.

### Аналіз вихідних файлів
|photo| 2.8 Mb | JPG |
|-----|--------|-----|
|scrin| 37 kb  | JPG |
|text | 12 kb  | JPG |

## 2. Стиснення без втрати якості (lossless)
### Завантажте кожне зображення в Squoosh.
### Використайте формати PNG (lossless) та WebP (lossless).
### Зафіксуйте зміни у вазі файлу після кожного перетворення.
### Переконайтеся, що якість зображення залишилася незмінною.

### Стиснення без втрати якості (lossless)
|Назва| PNG  |
|-----|------|
|photo|15.6mb|
|scrin|180kb |
|text |88.2kb|

|Назва|WebP  |
|-----|------|
|photo|644kb |
|scrin|13.7kb|
|text |10.7Kb|

## 3. Стиснення з втратою якості (lossy)
### Використайте формати MozJPEG, WebP (lossy) та AVIF.
### Виконайте стиснення на рівнях якості 100%, 75% та 50%.
### Зафіксуйте зміни розміру файлу.
### Визначте мінімальний рівень якості, при якому зображення залишається прийнятним.

### Стиснення з втратою якості (lossy)

|MozJPEG|  100   | 75   | 50   | min quality |
|-------|--------|------|------|-------------|
|photo  |4.25mb  |862kb |486kb |  101kb(8%)  |
|scrin  | 69kb   |16.3kb|10.9kb| 4.79kb(16%) |
|text   |45.6kb  |10.9kb|7.54kb| 7.43kb(49%) |

|WebP (lossy)|  100   | 75   | 50   | min quality |
|------------|--------|------|------|-------------|
|photo       |35.78mb |704kb |430kb |91.1kb(0%)   |
|scrin       |41.2kb  |13.7kb|10.6kb|2.68kb(0%)   |
|text        |26.4kb  |10.7kb|8.40kb|5.62kb(21%)  |

|AVIF | 100(99)|  75  | 50   | min quality |
|-----|--------|------|------|-------------|
|photo|3.05mb  |1.15mb|276kb | 16.7kb(0%)  |
|scrin|40.8kb  |17.7kb|9.25kb| 2.29kb(7%)  |
|text |28.7kb  |12.9kb|8.59kb| 4.84kb(30%) |

## 4. Оптимізація розміру відповідно до цільового використання
### Зменшіть розмір зображень відповідно до їхнього застосування:
### Для вебу: максимальна ширина 1200 px.
### Для мобільних пристроїв: максимальна ширина 600 px.
### Для Retina-дисплеїв: створіть 2x або 3x версію зображення.
### Зафіксуйте зміни у вазі файлу після кожного етапу.

|Назва| WEB  | Mobile |
|-----|------|--------|
|photo|118kb |36,7kb  |
|scrin|152kb |60.4kb  |
|text |69.5kb|27.9kb  |
## 5. Візуальний аналіз та висновки
### Порівняйте вихідні та оптимізовані зображення.
### Визначте, які формати та параметри оптимізації найкраще підходять для кожного типу зображень.
|Назва  | Порівняння вхідних та оптимізованих зображень               |
|-------|-------------------------------------------------------------|
|AVIF   |формат AVIF ідеально підходить для стискання файлів з текстом|
|WebP   |формат WebP ідеально підходить для стискання фото та файлів з мінімальною втратою якості|
|MozJPEG| формат MozJPEG ідеально підходить для стискання великих файлів з невеликою втратою якості, абож для максимального стиснення, ціною втати якості зображення|