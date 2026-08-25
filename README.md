# piroznoe.github.io

Public pages for the **Believe** iOS app. Static HTML, no build step, no dependencies.

**Before pushing: replace `you@example.com` in `privacy/index.html` with a real contact address**
(two places — the English and the Russian section).

## Pages

| URL | What it is |
|---|---|
| `/` | Minimal landing page |
| `/privacy/` | Privacy policy, language chosen from the browser |
| `/privacy/?lang=en` | Privacy policy, forced English |
| `/privacy/?lang=ru` | Privacy policy, forced Russian |

`/privacy/` holds both language versions in one document. A small inline script reads
`?lang=` first and falls back to `navigator.languages`; the CSS then hides the other version.
With JavaScript disabled nothing is hidden, so both versions stay readable. The language
buttons are plain links, so switching works without scripting too.

The pages set no cookies, load nothing from other hosts and store nothing in the browser.

## App Store Connect

Put `/privacy/?lang=en` in the Privacy Policy URL field of the English localization and
`/privacy/?lang=ru` in the Russian one. The app itself links to `/privacy/`, which resolves
the language on its own.
