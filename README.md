# RUSSIAN SEARCH — static GitHub Pages edition

A responsive, bilingual (Russian / English) static website built with HTML, CSS and vanilla JavaScript. No server, database, build step or runtime backend is required.

## Publish
1. Upload the contents of this folder to the root of your GitHub repository.
2. Open **Settings → Pages**.
3. Choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Save and wait for GitHub Pages to publish the site.

## Content management
The site uses [Pages CMS](https://app.pagescms.org/) as an external visual editor connected to GitHub.
1. Keep `.pages.yml` in the repository root.
2. Sign in to Pages CMS with GitHub and install its GitHub App.
3. Grant access only to the repository containing this site.
4. Edit **Исследования / Case studies** to add, update or remove publications.
5. Edit **Профиль и контакты** to update the biography, regions, email and Telegram handle.

There is no public admin page in this build. Open Pages CMS directly at https://app.pagescms.org/. GitHub Pages itself is static hosting and does not provide private server-side login or a database.

## Content
- Research entries: `data/projects.json`
- Public profile and contacts: `data/profile.json`
- Toolkit directory: `data/tools.json` (editable in Pages CMS under “Инструментарий / Tools”)
- CMS configuration: `.pages.yml`
- Styles: `assets/css.css` and `assets/brand.css`
- Behaviour and RU/EN translations: `assets/app.js`
- Uploaded media: `media/`

Case pages are rendered from `work/case.html?slug=...`. Demonstration entries are explicitly marked as fictional. Replace or remove sample entries before representing them as actual client work.

## Security
- Never commit GitHub passwords, Personal Access Tokens, OAuth secrets, private keys or client credentials.
- Enable GitHub 2FA or passkeys and keep recovery codes offline.
- Restrict the Pages CMS GitHub App to this one repository.
- Do not publish private client materials, leaked data, private communications or identifying information without a lawful basis and permission.
- A hidden URL is not access control. Do not store confidential content in a public GitHub Pages repository.

## Accessibility and responsive behaviour
- Mobile navigation supports tap-outside and Escape-to-close.
- Footer spacing accounts for mobile safe areas.
- Reduced-motion preferences are respected.
- Images use lazy loading where appropriate and fall back gracefully if an external image fails.


## Форматирование текста кейса и фотографии

В полях `body_ru` и `body_en` можно использовать HTML, который поддерживает редактор, либо Markdown. Если вставляете Markdown, сайт преобразует его при отображении:

- `## Заголовок` — заголовок раздела; `### Подзаголовок` — подзаголовок.
- `**жирный текст**` — жирное выделение; `*курсив*` — курсив.
- `- пункт` — маркированный список; `1. пункт` — нумерованный список.
- `> цитата` — цитата; `---` — разделитель.
- `[текст](https://example.com)` — ссылка.

### Фотография внутри публикации

1. Откройте в Pages CMS раздел **Media** и загрузите фотографию. Файлы должны находиться в папке `media`.
2. В тексте публикации в нужном месте добавьте строку:

   `![Описание фотографии](media/имя-файла.jpg)`

3. Сохраните публикацию и нажмите Save. После публикации фотография появится именно в этом месте текста.

Используйте короткие имена файлов латиницей, например `field-photo-01.jpg`. Для быстрой загрузки лучше подготовить изображения в WebP/JPEG и шириной около 1600 px.


## Инструментарий
Откройте Pages CMS → **Инструментарий / Tools** → создайте новую запись. Заполните название, категорию, описание, ссылку, платформу и при необходимости загрузите логотип через Media. Сохраните изменения. Карточки автоматически появятся на `tools.html`; поиск и фильтрация работают по названию, описанию, категории и платформе.
