# full-app

## Суть
Витрина интернет-магазина на headless-commerce: каталог, поиск и корзина, собранные поверх платформы Nacelle (headless commerce) на Preact. Лёгкий, быстрый сторефронт с компонентной библиотекой (Storybook) и офлайн-кэшем данных.

## Стек
- **Preact** (+ `preact-router`) — лёгкая альтернатива React.
- **Headless commerce:** `@nacelle/client-js-sdk` (данные каталога/контента).
- **Стейт/данные:** `zustand`, `localforage` (офлайн-кэш), `es-cookie`.
- **UI:** `keen-slider` (карусели), `classnames`, `uuidv4`, `lodash.*`.
- **Компоненты:** Storybook (`src/stories`), `mock-data` для разработки.

## Архитектура
Атомарная структура компонентов:
- `src/components/*` — `Atoms` (базовые), `Header`/`Navbar`, `Search`, `Cart`, `Main`, `Icons`, `Second`.
- `src/stories/*` — Storybook-истории компонентов.
- `src/mock-data/*` — моки для изолированной разработки.
- `src/types/*` — типы; состояние — `zustand`.

## Фичи
- **Каталог и контент:** загрузка через Nacelle SDK.
- **Поиск и корзина:** поисковая выдача и управление корзиной (zustand).
- **Карусели:** слайдеры товаров/баннеров (keen-slider).
- **Офлайн-кэш:** сохранение данных через localforage.
- **Компонентная библиотека:** Storybook для изолированной разработки и документации UI.

## Сложные места
- **Headless-commerce через Nacelle SDK.** Витрина отвязана от бэкенда магазина: данные (каталог/контент) приходят из Nacelle, UI полностью свой.
- **Preact вместо React.** Сборка и экосистема под Preact (роутер, совместимость) ради размера бандла и скорости.
- **Атомарный дизайн + Storybook.** Компоненты от `Atoms` вверх, с историями и моками — масштабируемая UI-библиотека.
- **Офлайн-кэш данных.** `localforage` для хранения ответов SDK и быстрого повторного рендера.

## Кейсы
- **«Headless-витрина на Preact + Nacelle».** Как отвязать сторефронт от бэкенда и держать его лёгким.
- **«Атомарная UI-библиотека со Storybook».** Компоненты от атомов до экранов с изолированной разработкой.
- **Статус: до ИИ.**

## Навыки
`Preact` · `preact-router` · `headless commerce (Nacelle SDK)` · `zustand` · `localforage (офлайн)` · `Storybook` · `atomic design` · `keen-slider` · `e-commerce`
