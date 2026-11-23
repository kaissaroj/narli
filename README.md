# Narli

Website for **Narli: Coloring Book for Kids** (iPhone and iPad), served at https://drawingapp.kaissaroj.com from this repo (GitHub Pages, `CNAME`).

- Home and the 12 book pages (`index.html`, `books/`), `sitemap.xml` and `robots.txt` are generated: run `python3 -I scripts/site-groups.py` (group pictures, only when the art changes) and `python3 -I scripts/site-build.py` in `kids-apps/coloring-book`. Don't edit them by hand.
- `fonts/` are Fredoka and Luckiest Guy (OFL), cut down to Latin with `pyftsubset <font> --unicodes="U+0020-007E,U+00A0,U+00A9,U+00B7,U+2013,U+2014,U+2018,U+2019,U+201C,U+201D,U+2026,U+203A,U+2022" --flavor=woff2 --layout-features='kern,liga'` (fontTools + brotli). If a page needs another character, add it there and to `unicode-range` in `site.css`.
- Cloudflare caches the pages for a day. After pushing a change, purge the cache for drawingapp.kaissaroj.com (Caching → Configuration → Purge Cache → Custom purge → Hostname) or wait a day.
- `help.html`, `privacy.html` and `terms.html` are written by hand.
- Pictures are © Niroj Subedi, all rights reserved. The site shows only small, watermarked group pictures, never single pages.
