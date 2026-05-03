# 🛍️ Shopping PWA — модуль покупок

Модуль вишлиста на GitHub Pages + Supabase.

## Файлы

```
shopping/
├── index.html     ← основной файл (всё в одном)
├── manifest.json  ← PWA манифест
├── sw.js          ← Service Worker (офлайн)
└── README.md
```

## Настройка

### 1. Ключи Supabase

В `index.html` найди строки:

```js
const SUPABASE_URL  = 'https://YOUR_PROJECT.supabase.co';
const SUPABASE_ANON = 'YOUR_ANON_KEY';
```

Замени на свои значения из Supabase → Settings → API.

### 2. GitHub Pages

1. Создай репозиторий (например `hub`)
2. Залей все файлы в папку `shopping/`
3. Settings → Pages → Source: `main` / `root`
4. Сайт будет доступен по адресу:  
   `https://USERNAME.github.io/hub/shopping/`

### 3. Иконки (опционально)

Добавь `icon-192.png` и `icon-512.png` в папку `shopping/`  
для красивого отображения при установке на телефон.

## База данных

Использует таблицу `purchases` с `module = 'shopping'`.  
Схема уже создана через SQL Editor в Supabase.

## Функции

- ✅ Добавление / редактирование / удаление
- ✅ Фото (загрузка в Supabase Storage → bucket `media`)
- ✅ Приоритет (высокий / средний / низкий)
- ✅ Статус (хочу / заказано / куплено)
- ✅ Теги (свободный ввод)
- ✅ Поиск и фильтрация
- ✅ Сортировка (приоритет / цена / дата)
- ✅ Статистика (сумма, количество)
- ✅ PWA (установка на телефон, офлайн-кеш)
- ✅ Демо-режим (без ключей)
