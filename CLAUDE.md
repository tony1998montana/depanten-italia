# Depanten Italia — Project Context

## Проект
SEO-сайт для итальянского бренда крема для суставов **Depanten**.

## Структура сайта (15 страниц)

| Файл | Ключевые слова | Приоритет |
|---|---|---|
| `index.html` | depanten, crema depanten, dolori articolari | 1.0 |
| `crema-depanten.html` | crema depanten, depanten crema | 0.9 |
| `depanten-farmacia.html` | depanten farmacia | 0.9 |
| `dolori-articolari.html` | dolori articolari, crema per articolazioni | 0.8 |
| `dolori-muscolari-articolari.html` | dolori muscolari e articolari diffusi in tutto il corpo | 0.8 |
| `proteina-c-reattiva.html` | proteina c reattiva alta e dolori articolari | 0.7 |
| `crema-per-articolazioni.html` | crema per articolazioni, crema per le articolazioni | 0.8 |
| `crema-acido-ialuronico.html` | crema acido ialuronico per articolazioni | 0.8 |
| `dolore-al-ginocchio.html` | dolore al ginocchio, dolore al ginocchio quando lo piego | 0.8 |
| `dolore-dietro-ginocchio.html` | dolore dietro al ginocchio | 0.7 |
| `artrosi-cura.html` | artrosi chi la cura, cura per artrosi, artrosi cura | 0.8 |
| `come-curare-artrosi.html` | come curare l'artrosi | 0.8 |
| `artrite-mani.html` | artrite alle mani rimedi, rimedi per artrite alle mani | 0.8 |
| `dolore-alla-schiena.html` | dolore alla schiena, dolore in fondo alla schiena | 0.8 |
| `dolore-schiena-parte-bassa.html` | dolore alla schiena parte bassa, dolore improvviso | 0.8 |

## Технические файлы
- `style.css` — основной stylesheet (темный плюм + золото + малиновый)
- `product.svg` — SVG иконка тюбика крема (без внешних зависимостей)
- `sitemap.xml` — sitemap для всех 15 страниц
- `robots.txt` — разрешает всё, указывает на sitemap

## Дизайн
- **Цвета:** `#2a0f1e` (plum bg), `#b7064d` (magenta CTA), `#ffcc19` (gold)
- **Шрифты:** Lobster (заголовки) + Roboto Condensed (текст) — Google Fonts
- **Кнопка:** `.btn-buy` — градиент малиновый, hover эффект
- **Продукт:** `product.svg` — custom SVG без everad CDN

## Деплой
- **GitHub:** https://github.com/tony1998montana/depanten-italia
- **Cloudflare Pages:** требует `CLOUDFLARE_API_TOKEN` (ожидает деплоя)

## Важно
- Нет форм (убраны по требованию)
- Нет упоминаний everad, affiliate tracking
- Кнопка покупки ведёт на `https://order.depanten.it/`
- Полная перелинковка между всеми страницами
- Schema.org Product markup на каждой странице
- Breadcrumbs на каждой странице

## Как задеплоить на Cloudflare Pages
```bash
# 1. Получить токен: https://dash.cloudflare.com/profile/api-tokens
# 2. Установить переменную:
export CLOUDFLARE_API_TOKEN=your_token_here
# 3. Создать проект и задеплоить:
cd /home/skip/Depanten
wrangler pages project create depanten-italia --production-branch master
wrangler pages deploy . --project-name depanten-italia
```
