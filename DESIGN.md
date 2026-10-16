---
version: alpha
name: BotForge Midnight
description: >-
  Тёмная витрина BotForge: полуночный фон, тонкая типографика, один синий акцент
  и россыпь цветных тегов-«этикеток» вокруг hero. Основа — style reference
  Copilot Money, адаптированный под кириллицу, WCAG AA и каталог Telegram-ботов.
colors:
  # Семантические алиасы — на них ссылаются компоненты
  primary: "#1c6cff"
  primary-hover: "#1558d6"
  surface: "#010d1e"
  on-surface: "#ffffff"
  link: "#5b93ff"
  error: "#ff4433"
  # Поверхности (от фона к самым «глубоким» колодцам; surface — уровень 1)
  midnight-canvas: "#000814"
  indigo-surface: "#001533"
  cobalt-surface: "#00215e"
  # Текст и линии
  paper-white: "#ffffff"
  fog: "#ccced0"
  mist: "#999ca1"
  steel-border: "#11263b"
  # Цвета тегов
  tag-coral: "#ff4433"
  tag-lime: "#00cc4b"
  tag-tangerine: "#ff8833"
  tag-hot-pink: "#ff33aa"
  tag-violet: "#9019e6"
  tag-sunflower: "#ffcc02"
  tag-sky: "#00acfe"
  tag-ember: "#ea687c"
  tag-olive: "#94ae43"
  tag-slate: "#5c6f8a"
typography:
  display:
    fontFamily: Inter Tight
    fontSize: 148px
    fontWeight: 600
    lineHeight: 0.9
    letterSpacing: -0.02em
  display-mobile:
    fontFamily: Inter Tight
    fontSize: 44px
    fontWeight: 600
    lineHeight: 0.95
    letterSpacing: -0.02em
  heading-lg:
    fontFamily: Inter Tight
    fontSize: 64px
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: -0.01em
  heading:
    fontFamily: Inter
    fontSize: 56px
    fontWeight: 100
    lineHeight: 1.2
    letterSpacing: -0.02em
  heading-sm:
    fontFamily: Inter
    fontSize: 38px
    fontWeight: 100
    lineHeight: 1.3
    letterSpacing: -0.02em
  subheading:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: 200
    lineHeight: 1.4
    letterSpacing: -0.01em
  eyebrow:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: 670
    lineHeight: 1
    letterSpacing: 0.04em
  eyebrow-mobile:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 670
    lineHeight: 1
    letterSpacing: 0.04em
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 300
    lineHeight: 1.6
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 300
    lineHeight: 1.4
    letterSpacing: -0.01em
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 300
    lineHeight: 1.4
    letterSpacing: 0em
  label-md:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
  label-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0.02em
  caption:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0em
rounded:
  image: 8px
  button: 16px
  input: 16px
  tag: 20px
  card: 24px
  container: 40px
  full: 9999px
spacing:
  space-4: 4px
  space-8: 8px
  space-12: 12px
  space-16: 16px
  space-20: 20px
  space-24: 24px
  space-28: 28px
  space-32: 32px
  space-40: 40px
  space-48: 48px
  space-56: 56px
  space-64: 64px
  space-80: 80px
  space-88: 88px
  space-112: 112px
  space-160: 160px
  page-max-width: 1200px
  gutter-mobile: 16px
  gutter: 40px
  section-gap-mobile: 80px
  section-gap: 120px
  card-padding: 24px
  element-gap: 16px
components:
  page:
    backgroundColor: "{colors.midnight-canvas}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
  divider:
    backgroundColor: "{colors.steel-border}"
    height: 1px
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    rounded: "{rounded.button}"
    padding: 12px
    height: 48px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-surface}"
  button-ghost:
    backgroundColor: transparent
    textColor: "{colors.on-surface}"
    typography: "{typography.label-md}"
    rounded: "{rounded.button}"
    padding: 12px
    height: 48px
  link:
    textColor: "{colors.link}"
    typography: "{typography.body-md}"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-padding}"
  card-featured:
    backgroundColor: "{colors.indigo-surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.card}"
    padding: "{spacing.card-padding}"
  card-glow:
    backgroundColor: "{colors.cobalt-surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.container}"
    padding: "{spacing.space-40}"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.input}"
    padding: 12px
    height: 48px
  input-helper:
    textColor: "{colors.mist}"
    typography: "{typography.caption}"
  input-error:
    textColor: "{colors.error}"
    typography: "{typography.caption}"
  chip-filter:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.fog}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 8px
  chip-filter-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-surface}"
  cart-drawer:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    width: 440px
  toast:
    backgroundColor: "{colors.indigo-surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.button}"
    padding: 16px
  eyebrow:
    textColor: "{colors.on-surface}"
    typography: "{typography.eyebrow}"
  tag-coral:
    backgroundColor: "{colors.tag-coral}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-lime:
    backgroundColor: "{colors.tag-lime}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-tangerine:
    backgroundColor: "{colors.tag-tangerine}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-hot-pink:
    backgroundColor: "{colors.tag-hot-pink}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-violet:
    backgroundColor: "{colors.tag-violet}"
    textColor: "{colors.paper-white}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-sunflower:
    backgroundColor: "{colors.tag-sunflower}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-sky:
    backgroundColor: "{colors.tag-sky}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-ember:
    backgroundColor: "{colors.tag-ember}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-olive:
    backgroundColor: "{colors.tag-olive}"
    textColor: "{colors.midnight-canvas}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
  tag-slate:
    backgroundColor: "{colors.tag-slate}"
    textColor: "{colors.paper-white}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.tag}"
    padding: 8px
---

# BotForge — дизайн-система

> Россыпь неоновых этикеток над полуночным хранилищем: чёрный холст, по которому под случайными углами плывут несколько ярких тегов, каждый светится, как табло вылетов в аэропорту.

Источник — style reference Copilot Money. Он адаптирован под BotForge: кириллица, WCAG AA, витрина Telegram-ботов вместо финансового приложения. Что изменено относительно источника и почему, описано в разделе «Отличия от источника» в конце файла. Токены в YAML выше нормативны, текст ниже объясняет, как их применять.

## Overview

Тёмная, тихая, почти монохромная витрина. Визуальный шум позволен в одном месте: россыпь ярких тегов вокруг hero. Теги подписаны названиями категорий и товаров из каталога (например «Запись», «Кафе», «Квиз», «Рассылки») и висят под небрежными углами. Список не захардкожен, он строится из данных.

Вторая опора стиля — типографика. Крупные заголовки набраны тонким Inter (weight 100), и страница выглядит так, будто напечатана на тёмной кальке. Hero-заголовок в Inter Tight SemiBold 148px держит структуру за счёт размера, а не жирности.

Единственный цветной призыв к действию — синий Signal Blue (`#1c6cff`). Глубину создают внутренние (inset) тени, а не внешние: интерфейс как будто вдавлен в тёмную плоскость, а не парит над ней.

Настроение: дружелюбная студия, а не корпорация. Плотность — свободная.

## Colors

Палитра: полуночные поверхности, белый текст, один синий акцент и десять «конфетных» цветов для тегов.

- **Midnight Canvas (`#000814`, `midnight-canvas`):** фон страницы и hero, базовый слой.
- **Deep Surface (`#010d1e`, `surface`):** первый уровень над фоном — карточки товаров, панель корзины, поля формы.
- **Indigo Surface (`#001533`):** второй уровень — вложенные панели, toast, выделенные карточки («Популярное»).
- **Cobalt Surface (`#00215e`):** самые глубокие колодцы, блок «Как это работает» (`card-glow`).
- **Paper White (`#ffffff`, `on-surface`):** заголовки, основной текст, иконки, рамка ghost-кнопки.
- **Fog (`#ccced0`):** второстепенный текст, неактивные чипсы фильтра.
- **Mist (`#999ca1`):** подсказки, метаданные, подписи к полям. Контраст на Deep Surface 7.08:1.
- **Steel Border (`#11263b`):** тонкие разделители между тёмными поверхностями. Для текста не годится: на фоне контраст 1.31:1.
- **Signal Blue (`#1c6cff`, `primary`):** только заливка главной кнопки, активный чипс, активный пункт меню. Белый текст на нём даёт 4.53:1. **Как цвет текста на тёмном фоне его не используют:** 4.44:1, ниже AA.
- **Primary Hover (`#1558d6`):** hover и pressed главной кнопки, контраст с белым 6.18:1.
- **Link (`#5b93ff`):** текстовые ссылки на тёмном фоне, 6.76:1.
- **Error (`#ff4433`):** текст ошибок валидации и рамка поля с ошибкой, 5.86:1 на фоне. Тот же цвет, что Tag Coral.

### Цвета тегов

Категории не привязаны к цветам по названию: каталог расширяется из админки, и в коде нет проверок вида «если категория X». Категория получает цвет по своей позиции в списке (`sortOrder`) из палитры `tagPalette`, по кругу. Те же цвета по кругу получают декоративные теги hero.

| № в `tagPalette` | Токен | Цвет | Текст на теге |
|---|---|---|---|
| 1 | `tag-sky` | `#00acfe` | Midnight |
| 2 | `tag-violet` | `#9019e6` | White |
| 3 | `tag-tangerine` | `#ff8833` | Midnight |
| 4 | `tag-lime` | `#00cc4b` | Midnight |
| 5 | `tag-coral` | `#ff4433` | Midnight |
| 6 | `tag-hot-pink` | `#ff33aa` | Midnight |
| 7 | `tag-ember` | `#ea687c` | Midnight |
| 8 | `tag-olive` | `#94ae43` | Midnight |

Два цвета в палитру не входят, у них служебная роль:

| Токен | Цвет | Текст на теге | Роль |
|---|---|---|---|
| `tag-sunflower` | `#ffcc02` | Midnight | Бейдж «Популярное», пометка «цена изменилась» в корзине |
| `tag-slate` | `#5c6f8a` | White | Нейтральный тег, «Недоступен» в корзине |

Цвет текста на теге выбран по контрасту, а не «всегда белый», как в источнике: белый на Sunflower даёт 1.51:1, на Lime 2.16:1. Тёмный текст на них же — 13.29:1 и 9.32:1.

## Typography

Две гарнитуры с полной кириллицей, обе бесплатные (SIL OFL):

- **Inter Tight** — только для display-заголовков (hero, крупные заголовки секций), weight 600. Заменяет Jokker из источника.
- **Inter** — всё остальное. Заменяет Matter Variable Thin и Matter SemiBold. Нужна вариативная версия: eyebrow использует weight 670.

Правила веса:

- **Weight 100–200** — только для текста от 24px и крупнее (`heading`, `heading-sm`, `subheading`). Это фирменный «шёпот».
- **Weight 300** — основной текст 14–18px (`body-*`). Тонкий 100 на тёмном фоне в мелком кириллическом кегле нечитаем.
- **Weight 400** — подписи кнопок, тегов, чипсов, мелкие подписи (`label-*`, `caption`).
- **Weight 600–670** — только display (Inter Tight) и eyebrow.

Адаптив: `display` (148px) — только на десктопе от 1024px. На мобильном используется `display-mobile` (44px), между ними — плавное `clamp()`. Так же `eyebrow` уменьшается до `eyebrow-mobile`. Длина строки основного текста — не больше 60ch.

Eyebrow (надзаголовок секции) пишется ПРОПИСНЫМИ с трекингом 0.04em: так он читается как табличка-указатель, а не как крик.

Шрифты подключаются локально (self-host через `@fontsource-variable/inter` и `@fontsource-variable/inter-tight`), а не с Google Fonts. Иначе IP посетителя уходит на серверы Google, а ТЗ требует хранить данные в РФ. Кроме того, не нужно расширять CSP.

## Layout

- Контейнер по центру, `page-max-width` 1200px. Боковые поля: 16px на мобильном (`gutter-mobile`), 40px на десктопе (`gutter`).
- Отступ между секциями: 80px на мобильном, 120px на десктопе.
- Шкала отступов кратна 4px (`space-4` … `space-160`). Внутренний отступ карточки 24px, зазор между элементами 16px.
- Ритм страницы: тёмная полоса на всю ширину → узкая колонка текста по центру → при необходимости рассыпанные декорации → следующая полоса. Секции различаются фоном (Midnight Canvas / Deep Surface), а не рамками.
- В hero нет двух колонок «текст + картинка» и нет сетки карточек. Hero — заголовок, подзаголовок и одна синяя кнопка (по умолчанию «Смотреть ботов», текст редактируется в админке), а вокруг теги.
- Сетка каталога по ТЗ: 1 колонка до 640px, 2 — до 1024px, 3–4 на десктопе.

## Elevation & Depth

Глубина строится на inset-тенях и смене тона поверхности. Внешних (drop) теней нет.

| Уровень | Тень | Где |
|---|---|---|
| Карточка, панель | `inset 4px 4px 16px -4px rgba(255,255,255,0.16), inset -4px -4px 16px -4px rgba(0,0,0,0.2), inset 4px 4px 8px 0 rgba(255,255,255,0.08), inset 1px 1px 1px -0.5px rgba(255,255,255,0.4)` | Карточка товара, панель корзины, поля формы |
| Pressed / active | `inset -4px -4px 16px -4px rgba(0,0,0,0.2)` | Нажатая кнопка, активная карточка |
| Glow | `inset 0 0 12px 0 rgba(38,113,217,0.08), inset 0 -4px 8px 0 rgba(0,0,0,0.32)` | Выделенные блоки на Indigo/Cobalt Surface |

Карточка дополнительно получает рамку 1px `steel-border`. Фон под панелью корзины и модалками затемняется (`rgba(0, 8, 20, 0.7)`) — это не тень, а оверлей, поэтому правило «без drop-теней» он не нарушает.

## Shapes

Скругления крупные и мягкие, но разные по ролям:

- **8px** — картинки (обложки товаров, галерея).
- **16px** — кнопки и поля ввода.
- **20px** — теги. Это не полная «пилюля», а скруглённый прямоугольник.
- **24px** — карточки и панели.
- **40px** — крупные контейнеры (блок «Как это работает»).
- **9999px** — чипсы фильтра, счётчик «− n +», бейдж корзины.

## Components

### Кнопки

- **Primary** (`button-primary`): заливка Signal Blue, белый текст `label-md`, скругление 16px, отступы 12px × 20px, высота 48px. Hover и pressed — `primary-hover`. Hover без подъёма и тени: кнопка плоская и уверенная. На экране одна такая кнопка: «Смотреть ботов», «В корзину», «Оформить заявку».
- **Ghost** (`button-ghost`): прозрачная, рамка 1px белая, белый текст. Вторичные действия: «Очистить корзину», кнопка примера работы (текст из `exampleLabel`: «Попробовать бота», «Посмотреть сайт»…).
- Фокус с клавиатуры: кольцо 2px `link` с отступом 2px. Убирать `outline` без замены нельзя.

### Теги

Скругление 20px, отступы 8px × 16px, `label-sm`, слева маленький эмодзи 14px. Цвет текста — по таблице в разделе Colors.

- **Декоративные теги в hero** повёрнуты на случайный угол от −12° до +12°, у соседних тегов углы разные, на сетку не выравниваются. Они чисто декоративные: `aria-hidden="true"`, без фокуса. На мобильном их 3–4 штуки, и они не перекрывают заголовок и кнопку.
- **Тег категории в карточке товара** не повёрнут: это информация, а не декор.

### Чипсы фильтра

`chip-filter`: Deep Surface, текст Fog, полное скругление. Активный (`chip-filter-active`) — Signal Blue с белым текстом. Это единственный случай, когда синяя заливка встречается не на кнопке.

### Карточка товара (сетка)

`card` с inset-тенью уровня «Карточка». Сверху обложка (скругление 8px), затем название `subheading`, краткое описание `body-sm` цветом Fog (2 строки, обрезка многоточием), цена `label-md` («9 900 ₽», «от 15 000 ₽», «от 1 500 ₽/час»). Снизу «В корзину» или счётчик «− n +». У товаров с ценой «от» счётчика нет: после добавления кнопка превращается в «В корзине ✓». Карточки из «Популярного» — `card-featured` на Indigo Surface.

### Поля формы (`/checkout`)

`input-field`: Deep Surface, рамка 1px `steel-border`, скругление 16px, высота 48px. Подпись над полем — `label-sm` белым, подсказка под полем — `input-helper` (Mist).

- Фокус: рамка `primary` и кольцо 2px `link`.
- Ошибка: рамка `error`, текст `input-error` под полем, `aria-invalid="true"` и `aria-describedby` на текст ошибки.
- Чекбокс согласия: квадрат 20px со скруглением 6px, в отмеченном состоянии — заливка `primary`.

### Панель корзины

`cart-drawer`: Deep Surface, ширина 440px, выезжает справа, на мобильном во весь экран. Строка позиции: мини-картинка 56px, название, цена, счётчик, сумма. Недоступная позиция получает тег `tag-slate` «Недоступен». Изменившаяся цена — пометка цветом `tag-sunflower`.

### Toast

`toast`: Indigo Surface, белый текст `body-sm`, скругление 16px, правый нижний угол (на мобильном — снизу на всю ширину). Действие внутри («Открыть») оформлено как `link`.

### Eyebrow

`eyebrow`: прописные, трекинг 0.04em, белый. Одна-три слова над заголовком секции, отступ до заголовка 16–24px.

### Логотип

Графический знак пока не утверждён, название «BotForge» рабочее. Самолётик Copilot Money не используем: он чужой и к тому же похож на логотип Telegram. Временно — словесный знак: `StoreSettings.name` набором Inter Tight 600 18px. Название подставляется из настроек, в вёрстке его нет.

### Скелетоны загрузки

Блоки на Indigo Surface с теми же скруглениями, что и итоговый контент. Анимация — медленное мерцание яркости. Если у пользователя включено `prefers-reduced-motion`, анимации нет.

## Do's and Don'ts

### Do

- Используйте `primary` (`#1c6cff`) как единственную цветную заливку для действий. Одна главная кнопка на экран.
- Выбирайте цвет текста на теге по таблице контраста (тёмный на светлых тегах), а не «всегда белый».
- Держите тонкие веса (100–200) для текста от 24px. Основной текст — 300, подписи — 400.
- Трекинг −0.02em для display и крупных заголовков, +0.04em для eyebrow.
- Разворачивайте декоративные теги hero на разные углы от −12° до +12°.
- Стройте глубину inset-тенями и сменой тона поверхности.
- Разделяйте секции сменой фона, а не рамками.
- Соблюдайте WCAG AA: 4.5:1 для обычного текста, 3:1 для крупного и для рамок полей.

### Don't

- Не используйте Signal Blue как цвет текста на тёмном фоне (4.44:1). Для ссылок есть `link`.
- Не ставьте белый текст на Sunflower, Lime, Sky, Tangerine, Olive и Ember: контраст ниже 3.5:1.
- Не используйте drop-тени на карточках, модалках и панелях.
- Не кладите цветные теги на светлый фон: яркие цвета работают только на полуночном.
- Не добавляйте второй брендовый цвет для кнопок и бейджей.
- Не выравнивайте декоративные теги по сетке и не давайте им одинаковый угол.
- Не используйте Inter Tight для основного текста, а тонкий Inter — для hero.
- Не добавляйте градиенты в фон: холст остаётся плоским.
- Не подключайте шрифты с Google Fonts — только self-host.

## Отличия от источника

Исходный style reference Copilot Money приведён к спецификации DESIGN.md (`@google/design.md`, версия формата `alpha`) и адаптирован под проект:

| Что | Было в источнике | Стало | Почему |
|---|---|---|---|
| Формат | Таблицы токенов в тексте, CSS-блоки | YAML front matter, разделы в порядке спецификации | Токены машиночитаемы: линтер, экспорт в Tailwind v4 `@theme` |
| Шрифты | Jokker, Matter Variable Thin, Matter-TRIAL SemiBold | Inter Tight, Inter | Jokker и Matter коммерческие, у Matter была trial-лицензия, которую нельзя использовать в проде. Inter и Inter Tight бесплатны и поддерживают кириллицу |
| Вес основного текста | 100 везде | 100–200 от 24px, 300 для основного текста | Читаемость кириллицы мелким кеглем на тёмном фоне |
| Текст на тегах | Всегда белый | Тёмный на светлых тегах | Белый на Sunflower — 1.51:1, на Lime — 2.16:1 |
| Ссылки, hover | Не заданы | `link` `#5b93ff`, `primary-hover` `#1558d6` | Signal Blue как текст на фоне — 4.44:1, ниже AA |
| Ошибки | Битые hex `#010d1`, `#00215`, `--section-gap: 80-120px` | `#010d1e`, `#00215e`, два токена отступа секций | Невалидный CSS |
| Скругление кнопки | 16px в компонентах и 9999px в подсказках для агентов | 16px | Противоречие в источнике |
| Мобильная версия | Не описана | `display-mobile`, `eyebrow-mobile`, `gutter-mobile` | ТЗ требует адаптив от 360px |
| Компоненты | Announcement bar, award badge, логотип-самолётик | Поля формы, чипсы, корзина, toast, скелетоны | Чего нет в ТЗ — убрано, что требует ТЗ — добавлено |
| OpenType-фичи | `cv03`, `ss07` и др. | Не заданы | Они относились к Matter и Jokker, у Inter те же коды означают другое |
