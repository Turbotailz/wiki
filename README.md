# wiki

Welcome to the LuckPerms wiki repository.

The wiki can be viewed on our website: https://luckperms.net/wiki

### Layout

* `/en/` — English wiki content as markdown. Folder tree = site URLs under `/wiki/`
* Additional locale folders (`/es/`, `/zh/`, …) can mirror `/en/` for community translations
* `/img/` — images embedded in wiki pages (shared across locales)

English examples:

* `/en/index.md` → https://luckperms.net/wiki
* `/en/features/web-editor/index.md` → https://luckperms.net/wiki/features/web-editor

When adding a language: copy the `en/` tree to `es/` (or another locale code), translate the markdown, keep the same relative paths, and open a PR. The website registers a `wiki_<locale>` Nuxt Content collection for each folder.


### License

The wiki content is licensed CC-BY-SA-4.0.
