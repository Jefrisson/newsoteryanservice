# Soteryan · BreachShield Service Intelligence Platform

Полноценная веб-витрина CRM-данных Soteryan с фирменной стилистикой BreachShield: тёмная тема, фирменный красно-вермильон, анимированные графики, интерактивные карточки.

## Что внутри

Single-page приложение на чистом HTML / CSS / JS. База — снимок `state.json` из CRM, встроен в страницу (без бэкенда).

### Разделы
- **Dashboard** — KPI с анимированными счётчиками, pipeline-чарт, donut по инвойсам, revenue by client, лента активности
- **Clients** — карточки с поиском и фильтром по индустрии, модал со связанными контактами/сделками/инвойсами/документами
- **Contacts** — карточки с фильтром по аккаунту
- **Deals & Projects** — Kanban + список, переключение видов, бейджи статусов и стадий
- **Tasks** — фильтры (All / Pending / Overdue / Done), подсветка просрочек
- **Invoices** — таблица с прогресс-барами оплаты, KPI сверху
- **Documents** — карточки с фильтром по категории (proposal / contract / brief / act)
- **Calendar** — месячная сетка с навигацией, sidebar с ближайшими событиями
- **POCs** — pipeline по 4 статусам (pending / approved / rejected / completed)
- **Conferences** — карточки с budget vs spent, модал с участниками и расходами
- **Reports** — 6 анимированных Chart.js графиков (funnel, donut, pie, horizontal bar, grouped bar)
- **Activity Log** — полная лента с фильтрами по типу

### Фишки UX
- Глобальный поиск по всем сущностям (Ctrl/Cmd + K)
- Анимации появления карточек, плавные переходы между видами
- Анимированные счётчики KPI
- Все Chart.js графики с easing-анимациями загрузки
- Модалы с кросс-навигацией (клиент → сделка → инвойс)
- Адаптив до мобильного (sidebar схлопывается)
- Бейдж нотификаций на POCs и Tasks

## Запуск

Просто открой `index.html` в браузере. Никакого build-шага и сервера не нужно.

Для GitHub Pages — загрузи в репозиторий и включи Pages из настроек.

## Структура данных

База в `data.json` (так же встроена в `index.html`):

| Сущность | Полей | Описание |
|----------|-------|----------|
| users | 9 | Пользователи системы (без passwordHash) |
| clients | 10 | Корпоративные аккаунты |
| contacts | 9 | Контакты у клиентов |
| projects | 12 | Сделки / проекты |
| tasks | 7 | Задачи |
| calendarEvents | 9 | События календаря |
| documents | 11 | Документы |
| invoices | 11 | Инвойсы |
| conferences | 14 | Конференции с участниками и расходами |
| pocs | 17 | Proof of Concept'ы |
| stages | 3 | Стадии воронки |
| activity | 4 | Лента активности |

## Стек

- HTML5 / CSS3 / Vanilla JS — без фреймворков
- [Chart.js 4](https://www.chartjs.org/) — графики
- Google Fonts: Space Grotesk + Open Sans

## Брендинг

Цвета и типографика повторяют сайт **soteryan-site**:
- `#950f18` — основной красный (charcoal)
- `#DC552A` — акцент вермильон
- Space Grotesk для заголовков, Open Sans для основного текста

Логотип BreachShield нарисован inline SVG (градиент + чек).
