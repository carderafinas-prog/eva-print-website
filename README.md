# Eva Print Pavlodar Website

Отдельный статический сайт интернет-магазина **Eva Print Pavlodar**.

## Назначение

Демо и последующая production-версия магазина футболок, мерча и индивидуальной печати.

Проект полностью отделён от Cardera и предназначен для самостоятельного деплоя через Cloudflare Pages / Workers & Pages.

## Стек

- HTML5
- CSS3
- Vanilla JavaScript
- без Node.js и обязательного build-step
- mobile-first responsive layout

## Точки входа

- `index.html` — страница магазина
- `css/style.css` — desktop/mobile интерфейс
- `js/app.js` — корзина, избранное, mobile menu, загрузка макета
- `data/products.json` — демонстрационный каталог
- `AGENTS.md` — обязательные правила разработки и UI baseline

## Cloudflare Pages

Рекомендуемые параметры:

- Framework preset: None
- Build command: оставить пустым
- Build output directory: `/` (корень репозитория)
- Production branch: `main`

## Статус

Первый baseline строится строго по утверждённым пользователем desktop/mobile эскизам Eva Print.
