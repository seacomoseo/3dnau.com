# 3dnau.com

[![3dnau.com](/assets/media/base/icon.png)](https://3dnau.com/)


## STEPS


### Local

- Design
  - GENERAL
    - `config.yml`
    - `data/*.{yml,md}`
  - CONTENT
    - `content/*`
      - SCRAP
        - Copy [this Spreadsheet Layout](https://docs.google.com/spreadsheets/d/1bJQaAFoBAwHhWz_WFRIHlkHoDmZZyT8H8NtdCnSTdaU)
        - First scrap with Screaming Frog and paste `url` and `title`
        - Second scrap with `IMPORTXML` formula in `content-start` tab
        - If need HTML content
          - Three scrap with `Web Scraper` chrome extension and paste in `content-scrap` tab
          - Copy `content-start` tab into `content-next` and get `body_code` (by `content-scrap`) with `VLOOKUP` formula
          - Copy `body_code` column to `body`, replace double quotes, [convert to Markdown](https://smalldev.tools/html-to-markdown-converter-online) and clean it
          - Paste in `file.md` in `./Downloads` and run `_tools/md-replaces.command`
          - Check `file_new.md` content:
            - headers: `^#`
            - images: `!\[.+?\)`
            - links: `(^|[^!])\[.+?\)`
            - internal links: `https?://(www\.)?example\.com`
          - Paste in sheet
        - Export to CSV like `./Downloads/file.csv` and run `_tools/csv-to-md.command`
        - Move files from `markdown_files` to `blog` project
  - Try in Safari and Firefox
  - Check in [W3 Validator](https://validator.w3.org/)
  - Check in [PageSpeed Insights](https://pagespeed.web.dev/)


### After client validate web


#### [Google Search Console](https://search.google.com/search-console)

- Add property
- Verify versions ⏩ `data/config.yml`
  - `google_analytics`
  - `google_site_verification`
  - `google_file_verification`
  - DNS:
    From: `@`
    DNS Record: `TXT`
    To: `google-site-verification=[google_site_verification]`
- Link with Analytics
- Add sitemap.xml


#### [Google My Business](https://business.google.com/)

- `Add company ⏩ ...` ⏩ whait 13 days to receive postal and insert code to verify


##### Delivery

Send to all collaborators next:

###### WhatsApp

```md
*ENTREGA WEB 3dnau.com*

Te dejo aquí este mensaje como referencia (también te lo paso por email con el asunto `ENTREGA WEB 3dnau.com`).

En el siguiente enlace tienes instrucciones sobre cosas referentes a tu sitio web (cómo modificar cosas, información extra, ect.):

https://seacomoseo.com/entrega/

No es necesario que lo veas, solo lo es si quieres hacer cosas por tu cuenta o si no estoy disponible.

¡Un saludo!
```

###### Mail

```
Asunto: ENTREGA WEB 3dnau.com
Cuerpo:
Te dejo aquí este email como referencia.

En el siguiente enlace tienes instrucciones sobre cosas referentes a tu sitio web (cómo modificar cosas, información extra, ect.):

https://seacomoseo.com/entrega/

No es necesario que lo veas, solo lo es si quieres hacer cosas por tu cuenta o si no estoy disponible.

¡Un saludo!
```
