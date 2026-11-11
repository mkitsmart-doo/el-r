# El-R — SEO & AEO edit guide

Edit these fields in `index.html` (and `404.html` where noted). After changing FAQ text on the page, update the matching FAQ JSON-LD block so they stay identical.

---

## 1. Page title (`<title>`)

**File:** `index.html` → `<head>`

**Current:**
```
El-R d.o.o. | Kućne i industrijske elektroinstalacije | Sjeverozapadna Hrvatska, Međimurje, Varaždin, Zagreb
```

**Tips:** ~50–60 characters ideal. Keep brand + main service + location. Used in Google tabs and search results.

---

## 2. Meta description

**File:** `index.html` → `<meta name="description">`

**Current:**
```
El-R d.o.o. iz Preloga: kućne i industrijske elektroinstalacije, inspekcija i servis u Međimurju i cijeloj sjeverozapadnoj Hrvatskoj. Certificirani električari — spojeno, provjereno, pouzdano.
```

**Tips:** ~140–160 characters. One clear sentence: who, what, where, proof.

---

## 3. Keywords (optional)

**File:** `index.html` → `<meta name="keywords">`

**Current:**
```
električar Prelog, elektroinstalacije Međimurje, industrijske elektroinstalacije, kućne elektroinstalacije, servis elektroinstalacija, električar Čakovec, električar Varaždin
```

**Tips:** Low ranking weight; keep short and real. Prefer phrases people actually search.

---

## 4. Canonical URL

**File:** `index.html` → `<link rel="canonical">`

**Current:** `https://www.el-r.hr/`

**404:** `404.html` uses `https://www.el-r.hr/404.html` + `noindex` (leave as-is).

---

## 5. Open Graph (Facebook / LinkedIn / WhatsApp)

| Field | Meta tag | Current |
|---|---|---|
| Title | `og:title` | `El-R d.o.o.  \| Kućne i industrijske elektroinstalacije`|
| Description | `og:description` | `Kućne i industrijske elektroinstalacije, inspekcija i servis. Spojeno, provjereno, pouzdano.` |
| URL | `og:url` | `https://www.el-r.hr/` |
| Image | `og:image` | `https://www.el-r.hr/assets/logo-dark.png` |
| Image alt | `og:image:alt` | `El-R d.o.o. logotip` |
| Site name | `og:site_name` | `El-R d.o.o.` |
| Locale | `og:locale` | `hr_HR` |

**Tips:** Share image ideally ~1200×630. Replace `logo-dark.png` with a dedicated OG image when you have one.

---

## 6. Twitter / X cards

| Field | Meta tag | Current |
|---|---|---|
| Card type | `twitter:card` | `summary_large_image` |
| Title | `twitter:title` | same as `og:title` |
| Description | `twitter:description` | same as `og:description` |
| Image | `twitter:image` | same as `og:image` |

Keep these in sync with Open Graph when you edit.

---

## 7. Local / geo

| Field | Meta / schema | Current |
|---|---|---|
| Region | `geo.region` | `HR-07` |
| Place | `geo.placename` | `Prelog` |
| Coordinates | `geo.position` / `ICBM` | `46.3381; 16.6156` |
| Schema lat/long | `Electrician` → `geo` | same |

Update coordinates if the exact pin should be the street address (Google Maps).

---

## 8. Business schema (`Electrician` JSON-LD)

**File:** `index.html` → first `<script type="application/ld+json">`

Editable fields:

| Field | Current |
|---|---|
| `name` | `El-R d.o.o.` |
| `url` | `https://www.el-r.hr/` |
| `telephone` | `+385989603524` |
| `email` | `info@el-r.hr` |
| `description` | Kućne i industrijske… sjeverozapadnoj Hrvatskoj. |
| `streetAddress` | `Ul. Kalmana Mesarića 45` |
| `postalCode` | `40323` |
| `addressLocality` | `Prelog` |
| `addressRegion` | `Međimurska županija` |
| `areaServed` | Prelog, Čakovec, Međimurje, Varaždin, Zagreb… |
| Hours | Mon–Fri `07:00`–`16:00` |
| `priceRange` | `$$` |
| `knowsAbout` | kućne / industrijske / inspekcija / servis |

**Optional later:** add `sameAs` with Google Business, Facebook, Instagram URLs.

---

## 9. FAQ schema (AEO — answers for Google / AI)

**File:** `index.html` → `FAQPage` JSON-LD **and** visible FAQ cards in `#faq`

Questions currently in schema (must match on-page text):

1. Gdje sve radite?
2. Izdajete li dokumentaciju o izvedenim radovima?
3. Kako mogu dobiti ponudu za radove?
4. Koliko traje izvedba elektroinstalacija?
5. Koje sve poslove obavljate?
6. Nudite li dugoročnu suradnju?
7. Popravljate li tuđe radove i stare instalacije?
8. Nudite li jamstvo na izvedene radove?

**Rule:** Change a FAQ on the page → copy the same Q&A into JSON-LD. Answer engines prefer short, direct first sentences.

---

## 10. Visible copy that ranks / answers

| What | Where | Notes |
|---|---|---|
| H1 slogan | Hero: Spojeno / Provjereno / Pouzdano | Brand-first; keep |
| Subline | `Kućne i industrijske elektroinstalacije` | Strong service phrase |
| Lead paragraph | Hero `.lead` | First place for “električar / Prelog / Međimurje” |
| Section H2s | Usluge, Zašto mi, Kontakt, FAQ | Keep clear and unique |
| Service cards | `#usluge` | H3 + short benefit + bullets |
| Contact blurb | `#kontakt` intro | Location phrase for local SEO |
| Image alts | Logo, hero electrician, footer logo | Describe subject + location lightly |
| Footer line | `Električar Prelog \| Međimurska županija` | Extra local signal |

---

## 11. 404 page

**File:** `404.html`

| Field | Current |
|---|---|
| Title | `Stranica nije pronađena \| El-R d.o.o.` |
| Description | `Tražena stranica ne postoji…` |
| Robots | `noindex` (keep) |

---

## 12. Crawl & AI files (usually leave alone)

| File | Role |
|---|---|
| `robots.txt` | Crawler rules + sitemap pointer |
| `sitemap.xml` | Indexable URLs (`lastmod` when content changes) |
| `llms.txt` | AI/agent entry point ([llmstxt.org](https://llmstxt.org/)) |

---

## Quick checklist after edits

1. Title + description still unique and accurate  
2. OG / Twitter titles & descriptions match  
3. FAQ page text = FAQ JSON-LD  
4. Phone / email / address match contact block + schema  
5. Canonical stays on `https://www.el-r.hr/`  
6. If you change services/FAQ/contact, update `llms.txt` too  
7. Bump `lastmod` in `sitemap.xml` when the homepage changes  
8. Test rich results: [Google Rich Results Test](https://search.google.com/test/rich-results)  
9. Re-submit sitemap / URL in Google Search Console when live  
