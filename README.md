# lenoriapp.com

The public website for **Lenori**, an iPhone and iPad app published by
DS Entertainment LLC.

Static HTML and CSS. No build step, no framework, no JavaScript, no
dependencies. Served by GitHub Pages at the apex domain `lenoriapp.com`.

## Why it is shaped this way

- **No JavaScript at all.** Nothing on the site needs it, and every script is
  something that can break, slow a page down, or watch a visitor.
- **No cookies, analytics, ads or third-party requests.** The typeface and
  every image are served from this origin. The privacy policy says the site
  contacts no one else, and that has to stay true.
- **One stylesheet**, with the palette taken from the Lenori app's own theme
  definitions rather than approximated. Rose Clay carries the site; Linen,
  Sage and Lagoon appear where a second voice is needed. If a theme is
  retuned in the app, retune it here to match.
- **Real screenshots.** The images in `images/` are captures of the shipping
  app, produced by the iOS project's own screenshot suite and resized for the
  web. Never replace them with mockups, and regenerate them when the app's
  appearance changes — a stale screenshot is a false claim about the product.

## Layout

```
index.html          landing page
features/           what the app does
privacy/            privacy policy
support/            help and contact
terms/              terms of use
404.html            served by GitHub Pages for unknown paths
styles.css          the whole design system
images/             screenshots, icons, Open Graph card
fonts/              Fraunces (see FONT-LICENSE.md)
CNAME               the custom domain
sitemap.xml         five routes
robots.txt          allows everything, points at the sitemap
.nojekyll           serve files as they are
```

## Editing

Open the file and edit it. There is nothing to install and nothing to compile.

To check it locally:

```
python3 -m http.server 8000
```

then visit <http://localhost:8000>. Clean URLs like `/features/` work because
each section is a directory with an `index.html`.

## Accuracy

The privacy page was written against the app itself — its entitlements,
privacy manifests, iCloud configuration, notification handling and purchase
handling — not from a template. The features page describes what ships,
including which themes are free and that Premium is not purchasable yet.
Keep both honest: if the app changes, these change with it.

The Terms page relies on Apple's Standard EULA for the app licence rather
than restating it. Sections that would need facts the owner has not supplied —
state of formation, mailing address, governing law, venue — are omitted rather
than filled with guesses.
