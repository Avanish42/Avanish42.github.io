# Avanish Singh Kushwah — Data & AI Engineer

Personal web résumé and showcase, hosted at **[avanish42.github.io](https://avanish42.github.io)**.

Principal Data Engineer & Databricks Certified Generative AI Engineer — 11+ years building
large-scale ETL/ELT pipelines and lakehouse platforms on Snowflake, PySpark, Python and cloud.

## What's here

- **`index.html`** — single-page showcase: hero, about, skills, certifications, experience timeline, contact.
  Self-contained (no build step): all styling is inline, with a certificate lightbox and scroll-reveal in vanilla JS.
- **`img/certificates/`** — certificate images (PNG) rendered from the source PDFs in `certificate/`.
- **`certificate/`** — source résumé PDF and certificate PDFs.
- **`about.html`** — redirects to `index.html#about` (kept for old inbound links).

## Certifications featured

- Databricks Certified **Data Engineer Associate** (Jan 2026 – Jan 2028)
- Databricks Certified **Generative AI Engineer Associate** (Aug 2026 – Aug 2028)
- Anthropic **Claude Code 101** — Certificate of Completion

## Updating the certificate images

The PNGs in `img/certificates/` are generated from the PDFs in `certificate/` using
[`pdf-to-img`](https://www.npmjs.com/package/pdf-to-img) (Node, no native deps):

```js
import { pdf } from "pdf-to-img";
const doc = await pdf("certificate/<file>.pdf", { scale: 2.5 });
for await (const page of doc) { /* write page (a PNG Buffer) to img/certificates/ */ }
```

## License

Code released under the [MIT](LICENSE) license. Original layout derived from the Start Bootstrap
*Creative* theme; the current site is a full rewrite.
