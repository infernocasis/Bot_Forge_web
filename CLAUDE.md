# BotForge — контекст проекта

Сайт-каталог Telegram-ботов: витрина + заявки + админка + уведомления в Telegram. Название «BotForge» рабочее (см. ТЗ).

Документы — источник истины, читать перед работой:
- [TZ-BotForge-MVP.md](TZ-BotForge-MVP.md) — что делаем (ТЗ v5).
- [architecture.md](architecture.md) — как устроен код: структура, правила зависимостей, деплой.
- [DESIGN.md](DESIGN.md) — дизайн-система: токены в YAML, правила в тексте.

## Технологии

| Слой | Технология | Версия | Заметки |
|---|---|---|---|
| Runtime | Node.js | ≥ 22.18 | Требуют `tsdown` и `vitest`. Docker: `node:22-slim` |
| Пакеты | npm workspaces | npm ≥ 11 | npm 10.9 падает на установке (`edgesOut`) — ставить через `npx npm@11 install` или обновить npm |
| Язык | TypeScript | 6.0.x (`~6.0.3`) | **Не 7.x**: `typescript-eslint` поддерживает `<6.1`. В TS 6 `types` по умолчанию `[]` — нужные `@types` перечислять явно |
| Фронт | Vue 3.5, Vue Router 5, Pinia 4 | | Две точки входа Vite: `index.html` (витрина), `admin.html` (админка, hash-роутер) |
| Сборка фронта | Vite 8, `@vitejs/plugin-vue` 6, `vue-tsc` 3 | | |
| Стили | Tailwind CSS 4 + `@tailwindcss/vite` | | Без `tailwind.config`. Тема `@theme` генерируется из DESIGN.md: `npm run design:export` |
| Шрифты | `@fontsource-variable/inter`, `@fontsource-variable/inter-tight` | | Только self-host, не Google Fonts |
| Markdown | `marked` 18 + `dompurify` 3 | | Любой HTML из Markdown — только через DOMPurify |
| Валидация | zod 4 | | Схемы общие для фронта и бэка в `@app/shared` |
| API | Fastify 5 + `fastify-type-provider-zod` 7 | | Плагины: `@fastify/helmet`, `cookie`, `rate-limit`, `multipart` |
| БД | PostgreSQL 16 + Prisma 7.10.1 | **точная** | Не 8.x: на npm `latest` = `8.0.0-rc`. `prisma`, `@prisma/client`, `@prisma/adapter-pg` держать на одной версии. Prisma 7: генератор `prisma-client`, подключение через `@prisma/adapter-pg`, `.env` сам не грузит |
| Telegram | grammY 1.x | | Long polling, в процессе API |
| Безопасность | `argon2` (argon2id), `file-type` (сигнатуры загрузок), `sharp` (пересжатие в WebP) | | |
| Бэк dev/build | `tsx` (dev, `--env-file=../../.env`), `tsdown` (прод-бандл) | | |
| Тесты | Vitest 5 | | |
| Качество | ESLint 10 (flat config) + `typescript-eslint` 8 + `eslint-plugin-vue` 10, Prettier 3 | | Стиль: без `;`, одинарные кавычки, ширина 100 |
| Дизайн-линт | `@google/design.md` | | В скриптах бинарь `designmd`: `design.md` на Windows открывается как файл |

## Структура

```
apps/web        — фронт (storefront/, admin/, shared/, styles/)
apps/api        — бэк (plugins/, modules/<name>/{routes,service}.ts, bot/, workers/, cli/, lib/), prisma/
packages/shared — @app/shared: zod-схемы, enum, pricing, DTO. Без Vue, Prisma и Node API
deploy/         — nginx-шаблон, Dockerfile'ы, скрипты
```

Импорт между `apps/web/src/storefront` и `apps/web/src/admin` запрещён (путь админки не должен попасть в бандл витрины).

## Команды

```
npm run dev            # api + web параллельно
npm run typecheck      # tsc / vue-tsc во всех пакетах
npm run lint           # ESLint + линт DESIGN.md
npm run test           # vitest
npm run format         # prettier
npm run design:export  # DESIGN.md → apps/web/src/styles/theme.css
npm run db:migrate     # prisma migrate dev
npm run db:seed
npm run admin:create
```

## Правила проекта

- Название магазина не хардкодить: `StoreSettings.name`, `STORE_NAME`, `ORDER_NUMBER_PREFIX` (architecture.md, 5.6).
- Категории и товары не сравнивать по названию/slug в коде — поведение только по полям (`priceType`, `isFeatured`, `isUpsell`, `exampleUrl`).
- Деньги — целые копейки, форматирование и итоги только через `pricing.ts` из `@app/shared`.
- `message` ошибок API — на английском, тексты UI — на русском.
- Файлы из PowerShell 5.1 писать с `-Encoding utf8`: `echo > file` создаёт UTF-16.
