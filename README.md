# piroznoe.github.io

Public pages for the **Believe** iOS app. Static HTML, no build step, no dependencies.

## Pages

| URL | What it is |
|---|---|
| `/` | Minimal landing page |
| `/privacy/` | Privacy policy, language chosen from the browser |
| `/privacy/?lang=en` · `/privacy/?lang=ru` | Privacy policy, forced language |
| `/support/` | Support page, language chosen from the browser |
| `/support/?lang=en` · `/support/?lang=ru` | Support page, forced language |

Each page holds both language versions in one document. A small inline script reads
`?lang=` first and falls back to `navigator.languages`; the CSS then hides the other version.
With JavaScript disabled nothing is hidden, so both versions stay readable. The language
buttons are plain links, so switching works without scripting too.

The pages set no cookies, load nothing from other hosts and store nothing in the browser.

## App Store Connect

Put `/privacy/?lang=en` in the Privacy Policy URL field of the English localization and
`/privacy/?lang=ru` in the Russian one; same for `/support/…` in the Support URL field.
The app itself links to `/privacy/` and `/support/`, which resolve the language on their own.
