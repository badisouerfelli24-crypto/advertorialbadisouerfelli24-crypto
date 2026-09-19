# Advertorial Editor

A single-file editor for building advertorial landing pages. Open `index.html` in a browser, no build step needed.

## Features

- Dashboard to create, name, duplicate and delete multiple advertorials
- Hero, body, and call-to-action editors with a visual (WYSIWYG) article editor
- Text Style panel: fonts, sizes, weights, alignment, line spacing
- Right-to-left mode with Arabic fonts (Cairo, Tajawal, Almarai, Noto Kufi/Naskh Arabic, Amiri)
- Images placed beside the article, moved and resized with corner handles
- Automatic image compression

## Running locally

Open `index.html` directly in a browser, or serve the folder:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Important notes

- **Storage is per browser.** Content is saved in the browser's `localStorage`. It is not in this repo and does not sync between browsers or devices. Clearing site data deletes it.
- **Not a secure admin.** The login is a client-side convenience only. The default password (`admin123`) is visible in the source. Change it in Settings, and do not host this editor publicly as a protected admin area.
- **Publishing.** GitHub Pages serves only the `docs/` folder, never the editor. To publish, open the editor locally, click **Save** then **Download Page**, and put the file in `docs/` (`docs/index.html` is the home page; others go in `docs/<name>.html`).
- **No secrets.** This project uses no API keys. Never commit `.env` files. They are ignored by `.gitignore`.
