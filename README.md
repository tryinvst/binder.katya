# Екатерина Биндер — лендинг ведущей

Одностраничный сайт: статичный HTML без сборки и зависимостей. Шрифты подключаются с Google Fonts, всё остальное лежит в репозитории.

## Структура

```
index.html     — страница (стили и скрипт внутри)
favicon.svg    — иконка вкладки
img/           — изображения (webp)
.nojekyll      — отключает обработку Jekyll на GitHub Pages
```

## Как опубликовать на GitHub Pages

1. Создайте на GitHub новый репозиторий, например `binder-landing`.
2. Загрузите в него содержимое этой папки (не саму папку): на странице репозитория нажмите **Add file → Upload files** и перетащите `index.html`, `favicon.svg`, `README.md`, `.nojekyll` и папку `img`. Нажмите **Commit changes**.
   - Файл `.nojekyll` скрытый. Если браузер его не показывает, его можно пропустить, сайт работает и без него.
3. Откройте **Settings → Pages**. В разделе **Build and deployment** выберите **Source: Deploy from a branch**, ветку **main** и папку **/ (root)**, нажмите **Save**.
4. Через 1–2 минуты сайт будет доступен по адресу `https://<ваш-логин>.github.io/binder-landing/`.

Через командную строку то же самое:

```bash
cd binder-github
git init
git add .
git commit -m "Лендинг Екатерины Биндер"
git branch -M main
git remote add origin https://github.com/<ваш-логин>/binder-landing.git
git push -u origin main
```

## Свой домен

В **Settings → Pages → Custom domain** укажите домен (например `katerinabinder.ru`) и у регистратора домена добавьте записи:

- для корневого домена — четыре записи `A`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`;
- для `www` — запись `CNAME` на `<ваш-логин>.github.io`.

После проверки включите **Enforce HTTPS**.

## Как поменять ссылки и тексты

Всё редактируется прямо в `index.html` (можно через карандаш на GitHub). Ссылки на ролики Rutube, Telegram, ВКонтакте, MAX и Instagram ищутся поиском по `href="https://`.
