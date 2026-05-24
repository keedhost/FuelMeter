<div align="center">
  <img src="logo.svg" width="72" alt="Fuel Meter logo">
  <h1>Fuel Meter</h1>
  <p>Калькулятор витрати палива та вартості поїздки для України</p>

  [![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-live-E85D04?style=flat-square&logo=github)](https://keedhost.github.io/FuelMeter/)
  [![License: MIT](https://img.shields.io/badge/License-MIT-00D47E?style=flat-square)](https://opensource.org/license/mit)
  [![HTML](https://img.shields.io/badge/HTML%20+%20CSS%20+%20JS-single%20file-4A90D9?style=flat-square)](index.html)
</div>

---

## Про застосунок

**Fuel Meter** — безкоштовний однофайловий вебзастосунок без реклами та реєстрації. Допомагає швидко розрахувати, скільки палива і грошей потрібно на поїздку, побудувати маршрут на карті та дізнатися, скільки разів доведеться зупинитись на АЗС.

Працює прямо в браузері — без серверів, без встановлення, без збору даних.

🔗 **[keedhost.github.io/FuelMeter](https://keedhost.github.io/FuelMeter/)**

---

## Можливості

### Калькулятор — три режими розрахунку

| Режим | Що вводиш | Що отримуєш |
|---|---|---|
| **км → л / ₴** | Відстань, розхід, ціна | Літри палива, вартість поїздки |
| **₴ → км** | Бюджет, розхід, ціна | Кілометраж, кількість літрів |
| **л → км** | Кількість літрів, розхід | Кілометраж, вартість |

Для всіх режимів додатково розраховується **кількість зупинок на АЗС** (якщо вказано ємність бака).

### Типи палива з актуальними цінами

- А-92 · А-95 · А-98 · Дизель · Автогаз
- Ціни **автоматично оновлюються** з [minfin.com.ua](https://minfin.com.ua) при кожному відкритті
- Якщо автооновлення недоступне — вбудовані дефолтні значення

### Маршрут на карті

- Введи назву міста або адреси — автодоповнення знаходить місце через **Nominatim / OpenStreetMap**
- Підтримка **необмеженої кількості проміжних точок**
- Маршрут прокладається через **OSRM** — безкоштовний роутинг без ключів API
- Відстань автоматично підставляється в калькулятор
- Карта на темних тайлах **CartoDB Dark / Light** залежно від теми

### Додатково

- **Поділитись розрахунком** — кнопка генерує URL з усіма параметрами (режим, паливо, маршрут, тема). Отримувач бачить точно ту саму картину
- **Темна / світла тема** — перемикається одним кліком, зберігається між сесіями
- **Адаптивний дизайн** — коректно працює на смартфоні та ноутбуці
- **SEO-оптимізація** — Open Graph, Twitter Card, JSON-LD schema для Google Rich Results

---

## Технології

| Що | Чим |
|---|---|
| Інтерфейс | HTML5 + CSS3 + Vanilla JS (без фреймворків) |
| Карта | [Leaflet.js 1.9.4](https://leafletjs.com/) |
| Тайли | CartoDB Dark Matter / Positron |
| Геокодування | [Nominatim](https://nominatim.org/) (OpenStreetMap) |
| Маршрути | [OSRM](http://project-osrm.org/) |
| Ціни на паливо | [minfin.com.ua](https://minfin.com.ua) через CORS-проксі |
| Шрифти | Bebas Neue · Barlow Condensed · Space Mono (Google Fonts) |
| Хостинг | GitHub Pages |

Весь застосунок — **один файл `index.html`**. Ніякого бекенду, ніяких залежностей npm, ніяких збірок.

---

## Структура проєкту

```
FuelMeter/
├── index.html      # Весь застосунок
├── logo.svg        # Логотип (favicon + брендинг)
├── og-image.png    # Превʼю для соціальних мереж (1200×630)
└── README.md
```

---

## Локальний запуск

Достатньо відкрити `index.html` у браузері — серверна частина не потрібна.

```bash
git clone https://github.com/keedhost/FuelMeter.git
cd FuelMeter
open index.html        # macOS
# або
start index.html       # Windows
```

> Геокодування та маршрути потребують інтернет-з'єднання (зовнішні API).

---

## Деплой на GitHub Pages

1. Форкни або клонуй репозиторій
2. Перейди до **Settings → Pages**
3. Вибери гілку `main`, кореневу директорію `/`
4. Збережи — застосунок з'явиться за адресою `https://<username>.github.io/FuelMeter/`

---

## Автор

**Андрій Кондратьєв** — [LinkedIn](https://www.linkedin.com/in/andriy-kondratyev/) · [GitHub](https://github.com/keedhost)

---

## Ліцензія

Розповсюджується під ліцензією [MIT](https://opensource.org/license/mit). Використовуй, модифікуй, поширюй вільно.
