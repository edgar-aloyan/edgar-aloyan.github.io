# CLAUDE.md — Project Context

## Что это

Личный сайт-резюме Эдгара Алояна, хостится через GitHub Pages по адресу `edgar-aloyan.github.io`.
Одна HTML-страница, оформленная как лист A4. Цель — CV, которое одинаково хорошо выглядит в браузере и при печати/сохранении в PDF.

## Стек

- Vanilla HTML / CSS / JS — без фреймворков
- FontAwesome 6 (локально, `icons/fa6_1_1/`)
- Google Fonts (Raleway, Rubik, Old Standard TT)
- `@media print` для генерации PDF прямо из браузера (`window.print()`)
- Тёмная тема через `dark.css`, управляется через `prefers-color-scheme`

## Ключевые файлы

| Файл | Роль |
|------|------|
| `index.html` | Весь контент CV |
| `style.css` | Основные стили + `@media print` |
| `dark.css` | Переопределения для тёмной темы |
| `script.js` | Тёмная тема, `screenshotMode`, `rotate` |

## Что уже сделано

- `pdf-mode.css` удалён — стили перенесены в `@media print` в `style.css`
- Кнопка "Save as PDF" вызывает `window.print()`, статичный PDF удалён
- Контакты (LinkedIn, GitHub, email, телефон) всегда видны на странице
- Исправлен typo `Machinary → Machinery`
- Убрана формулировка `"unreachable & unhackable"` → `"hardened, privacy-first"`
- Добавлена ссылка на GitHub (`https://github.com/edgar-aloyan`)

## Что можно сделать дальше

### Контент (нужны данные от владельца)
- [ ] Добавить метрики в описания опыта — размер команд, объёмы данных, масштаб систем
- [ ] Сгруппировать навыки по категориям (Languages / Cloud & Infra / Security / Databases / Networking)
- [ ] Обновить profession title — сейчас `Computer Science Engineer`, хотя опыт ближе к Cybersecurity / CTO

### Техническое
- [ ] SEO meta-теги: `description`, `og:title`, `og:image`, `og:url`, Schema.org `Person`
- [ ] Git-теги для версионирования CV (`git tag v2025.01`)
- [ ] Оптимизировать `avatarShot2.jpeg` → WebP
- [ ] Google Fonts хостить локально (сейчас подгружаются с внешнего сервера)

### Дизайн
- [ ] Адаптивность под мобильные (сейчас viewport зафиксирован `initial-scale=0.5`)

## Соглашения

- Коммиты в формате `fix:`, `feat:`, `refactor:` + описание
- Контент редактируется только в `index.html`
- Стили для печати — только в `@media print` внутри `style.css`
- Тёмная тема — только в `dark.css`
