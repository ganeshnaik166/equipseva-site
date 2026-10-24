# equipseva.com

The public website for EquipSeva. GitHub Pages serves it from the root of the `main` branch, under the custom domain equipseva.com, behind Cloudflare.

The pages are plain static files: no build step, no Jekyll (`.nojekyll`), no web fonts, no scripts. Push to `main` and Pages publishes the change.

| Path | What it is |
|---|---|
| `index.html` | Home page: the NABH equipment file offer |
| `privacy/`, `terms/`, `refunds/`, `licenses/`, `delete-account/` | Legal pages. The text was copied verbatim on 2026-10-24 from the earlier site (ganeshnaik166/equipseva-android, `docs/launch/*.md` at 3f01d417). It still describes the EquipSeva app. Changes to it are for the lawyer. |
| `privacy-policy/`, `tos/`, `terms-of-service/`, `refund/`, `refund-policy/`, `open-source/`, `open-source-licenses/`, `launch/…` | Redirects from older URLs to the pages above. Keep them: old links and listings point at them. |
| `.well-known/assetlinks.json` | Android App Links file for the EquipSeva app. Byte-identical to the app repo's copy. |
| `auth/reset.html`, `auth/reset.css`, `auth/reset.js` | The password-reset page that the app's reset emails open (`/auth/reset`). Built in the app repo (`docs/auth`) and copied here as built. It contains the Supabase publishable key, so rebuild it if that key is rotated. |
| `site.css` | Styles for every page |
| `og-equipment-file.jpg` | Link-preview image (1200×630) |
| `404.html`, `robots.txt`, `sitemap.xml`, `favicon.svg` | Standard site files |

Rule: only public pages go in this repo. Internal documents never do.
