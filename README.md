# Портфолио Flutter Developer - Abduqahhor Yakubi

Современное резюме-лендинг с полной оптимизацией для скорости работы, SEO и PWA.

## 🚀 Реализованные оптимизации

### 1. **SEO оптимизация**
- ✅ Расширенные meta-теги (title, description, keywords)
- ✅ Open Graph для социальных сетей (Facebook, VK)
- ✅ Twitter Cards
- ✅ Structured Data (JSON-LD) для поисковых систем
- ✅ Robots.txt и Sitemap.xml
- ✅ Canonical URL

### 2. **Производительность**
- ✅ Lazy loading для всех изображений
- ✅ Preload для критических ресурсов
- ✅ Preconnect для внешних шрифтов
- ✅ Service Worker для кэширования
- ✅ Оптимизация загрузки YouTube iframe

### 3. **PWA (Progressive Web App)**
- ✅ Web App Manifest
- ✅ Service Worker с кэш-стратегией
- ✅ Offline поддержка
- ✅ Возможность установки на устройство

### 4. **Безопасность и кэширование**
- ✅ .htaccess с GZIP сжатием
- ✅ Browser caching для статических ресурсов
- ✅ Security headers (X-Content-Type-Options, X-Frame-Options, X-XSS-Protection)

## 📁 Структура файлов

```
resume/
├── index.html          # Главная страница
├── manifest.json       # PWA манифест
├── sw.js              # Service Worker
├── robots.txt         # Инструкции для поисковых ботов
├── sitemap.xml        # Карта сайта
├── .htaccess          # Конфигурация Apache (сжатие, кэширование)
└── assets/            # Изображения проектов
```

## 🌐 Развертывание

### Локальная разработка
```bash
# Просто откройте index.html в браузере
# Или используйте локальный сервер:
python -m http.server 8000
# или
npx http-server
```

### Развертывание на хостинге

1. **Загрузите все файлы на хостинг**
2. **Убедитесь, что .htaccess работает** (для Apache)
3. **Измените URL в следующих местах:**
   - `index.html`: замените `https://yakubiam.dev/` на ваш домен
   - `manifest.json`: обновите start_url
   - `sitemap.xml`: обновите URL

### Важные настройки

**Для Apache:**
- Файл `.htaccess` уже настроен
- Включено GZIP сжатие
- Настроено кэширование браузера

**Для Nginx:**
Добавьте в конфигурацию:
```nginx
# GZIP сжатие
gzip on;
gzip_types text/plain text/css application/json application/javascript text/xml application/xml;

# Кэширование
location ~* \.(jpg|jpeg|png|gif|ico|css|js|woff2)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
}
```

## 🎯 Проверка производительности

После развертывания проверьте сайт:
- [Google PageSpeed Insights](https://pagespeed.web.dev/)
- [GTmetrix](https://gtmetrix.com/)
- [WebPageTest](https://www.webpagetest.org/)

## 📊 SEO проверка

- [Google Search Console](https://search.google.com/search-console)
- [Rich Results Test](https://search.google.com/test/rich-results)
- [Open Graph Debugger](https://developers.facebook.com/tools/debug/)

## 🔧 Кастомизация

### Изменение мета-тегов
Отредактируйте в `index.html`:
- Title и description
- Open Graph теги
- Twitter Cards
- Structured Data (JSON-LD)

### Добавление проектов
1. Добавьте изображение в папку `assets/`
2. Добавьте карточку проекта в секцию `#projects`
3. Создайте модальное окно с деталями
4. Добавьте обработчик в JavaScript

### Обновление Service Worker
При изменении файлов обновите версию кэша:
```javascript
const CACHE_NAME = 'yakubi-portfolio-v2'; // увеличьте версию
```

## 📱 PWA установка

Пользователи могут установить сайт как приложение:
- **Android/Chrome**: Кнопка "Установить приложение"
- **iOS/Safari**: "Добавить на домашний экран"
- **Desktop**: Иконка установки в адресной строке

## ⚡ Оптимизация изображений

Рекомендуется сжать изображения перед загрузкой:
- Используйте WebP формат для лучшего сжатия
- Инструменты: [TinyPNG](https://tinypng.com/), [Squoosh](https://squoosh.app/)

## 🔄 Обновления

При обновлении контента:
1. Измените версию в Service Worker
2. Обновите дату в sitemap.xml
3. Очистите кэш браузера для тестирования

## 📞 Контакты

- Telegram: [@yakubiam](https://t.me/yakubiam)
- Behance: [yakubiam](https://www.behance.net/yakubiam)

---

**Версия:** 1.0  
**Последнее обновление:** Октябрь 2025

