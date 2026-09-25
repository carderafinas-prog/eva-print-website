# Eva Print Pavlodar Website

Отдельный сайт интернет-магазина **Eva Print Pavlodar**.

## Назначение

Демо и последующая production-версия магазина футболок, мерча и индивидуальной печати.

Проект полностью отделён от Cardera и разворачивается как самостоятельное приложение через Cloudflare Pages / Workers & Pages.

## UI baseline

Утверждённые пользователем desktop/mobile эскизы от 25.09.2026 являются обязательным визуальным baseline. Перед изменением интерфейса читать `AGENTS.md`.

## Текущая структура

- `index.html` — самодостаточная версия магазина: HTML + CSS + JavaScript + встроенные demo-assets;
- `AGENTS.md` — правила проекта и зафиксированный UI baseline;
- `_headers` — security headers для Cloudflare Pages.

На первом этапе страница намеренно self-contained, чтобы при первом подключении Cloudflare не возникли сломанные пути к изображениям. После визуального приёмочного прогона код можно разделить на `css/`, `js/`, `assets/`, не меняя внешний вид.

## Cloudflare Pages

Для первого деплоя:

- Production branch: `main`
- Framework preset: **None**
- Build command: **пусто**
- Build output directory: **корень репозитория**
- Root directory: **/**

Cloudflare должен публиковать `index.html` напрямую.

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
