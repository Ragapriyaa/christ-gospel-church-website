# Christ Gospel Church, Coimbatore: website

A plain HTML, CSS and JavaScript site in English and Tamil. There is no build step and no database, so it can be uploaded to any web host as it is.

## See it on your computer

```bash
node tools/serve.mjs
```

Then open http://localhost:5173. Use this rather than double-clicking `index.html`, because YouTube's players refuse to run from a file on disk.

## The live website

The site is live at https://ragapriyaa.github.io/christ-gospel-church-website/ through GitHub Pages. Every push to the `main` branch updates it within a few minutes.

## Where to change things

| To change | Edit |
| --- | --- |
| Address, phone numbers, WhatsApp number, service time, logo | `assets/js/config.js` |
| UPI or bank details (they appear on the Connect page once filled in) | `giving` in `assets/js/config.js` |
| Special service dates | `events` in `assets/js/config.js` |
| Daily verses | `verses` in `assets/js/config.js` |
| English wording | the HTML page itself |
| Tamil wording | `assets/js/i18n-ta.js` |
| Colours and fonts | top of `assets/css/styles.css` |

## Keeping videos current

The "Today's meditation" and "Latest service" players always show the newest upload, with no work needed. The searchable library is a saved list, so refresh it now and then:

```bash
node tools/update-videos.mjs
```

Then upload `assets/js/videos.js` again.

