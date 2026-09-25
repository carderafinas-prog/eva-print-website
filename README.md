# Eva Print Pavlodar Website

Отдельный сайт интернет-магазина **Eva Print Pavlodar**.

## Назначение

Демо и последующая production-версия магазина футболок, мерча и индивидуальной печати.

Проект полностью отделён от Cardera и разворачивается как самостоятельное приложение через Cloudflare Pages / Workers & Pages.

## UI baseline

Утверждённые пользователем desktop/mobile эскизы от 25.09.2026 являются обязательным визуальным baseline. Перед изменением интерфейса читать `AGENTS.md`.

## Текущая структура

- `index.html` — исходный self-contained baseline;
- `public/index.html` — файл, который публикует Cloudflare Workers Static Assets;
- `wrangler.jsonc` — конфигурация Workers Builds / Static Assets;
- `AGENTS.md` — правила проекта и зафиксированный UI baseline;
- `_headers` — security headers для Cloudflare Pages.

На первом этапе страница намеренно self-contained, чтобы при первом подключении Cloudflare не возникли сломанные пути к изображениям. После визуального приёмочного прогона код можно разделить на `css/`, `js/`, `assets/`, не меняя внешний вид.

## Cloudflare Workers Builds

Для текущего Cloudflare Workers & Pages мастера:

- Production branch: `main`
- Project name: `eva-print-website`
- Build command: **пусто**
- Deploy command: `npx wrangler deploy`
- Preview command: `npx wrangler preview`

`wrangler.jsonc` публикует статические файлы из `public/`. Основная production-страница: `public/index.html`.

## Функции демо

- desktop layout по утверждённому образцу;
- отдельная mobile-компоновка;
- карточки товаров;
- избранное;
- корзина;
- загрузка макета для своего принта;
- блок категорий;
- четыре шага заказа;
- Instagram CTA;
- нижний продающий CTA.

Реальная оплата и отправка заказа пока не подключены.
