# The Sketch Buyer Ledger

A searchable, filterable directory of 798 fashion sketch buyers, licensors, and platforms — built as a single static HTML file with zero backend and zero dependencies beyond two Google Fonts.



---

## What it is

A trade reference tool for fashion sketch artists doing outreach: marketplaces, B2B wholesale platforms, luxury houses, contemporary brands, licensing agencies, department stores, and more — organized into 20 categories, each sourced from the original **Fashion Sketch Artist Directory** (May 2026, 798 verified contacts).

## Features

- **Full-text search** across company name, notes, website, and category
- **Category filter** — dropdown select or clickable color-swatch chips (20 categories, each with its own swatch color)
- **Sort** — directory order, A→Z, Z→A, or grouped by category
- **CSV export** — downloads whatever's currently filtered, ready to paste into a spreadsheet or CRM
- **Direct links** — every row opens straight to the company's site in a new tab
- Fully responsive, keyboard-accessible, respects `prefers-reduced-motion`

## Stack

- Plain HTML / CSS / vanilla JS — no framework, no build step
- Data embedded inline as JSON (`~798` records, ~145KB) — no fetch calls, works fully offline
- Fonts: [Fraunces](https://fonts.google.com/specimen/Fraunces) (display), [Inter](https://fonts.google.com/specimen/Inter) (body), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (data/labels), loaded from Google Fonts CDN

## Running it locally

Just open `index.html` in a browser. That's it — no server required.

```bash
open index.html      # macOS
start index.html      # Windows
```

## Deploying

Works as-is on any static host. For GitHub Pages:

```bash
git init
git add index.html README.md
git commit -m "Add Sketch Buyer Ledger"
git branch -M main
git remote add origin https://github.com/<your-username>/sketch-buyer-ledger.git
git push -u origin main
```

Then enable Pages in the repo settings (`Settings → Pages → Deploy from branch → main → /root`).

## Data

All 798 entries live inline in `index.html` inside a `<script type="application/json">` tag, so the page never makes a network request to load data. To update or re-source the directory:

1. Edit the source data (company / website / notes / category)
2. Re-generate the JSON array
3. Replace the contents of the `#directory-data` script tag

Each record has this shape:

```json
{
  "id": 1,
  "section": 1,
  "category": "Online Marketplaces & Selling Platforms",
  "company": "Etsy",
  "website": "www.etsy.com",
  "notes": "Handmade & digital art marketplace — sell sketch prints/files"
}
```

## Categories (20)

1. Online Marketplaces & Selling Platforms
2. B2B Wholesale & Trade Platforms
3. Luxury & High-End Fashion Houses
4. Contemporary & RTW Fashion Brands
5. Mass Market, Fast Fashion & Retail Buyers
6. Freelance & Design Licensing Platforms
7. Textile, Pattern & Print Licensing
8. Department Store Design Buyers
9. Activewear, Athleisure & Sportswear Buyers
10. Bridal, Formal & Occasion Wear Buyers
11. Children's & Teen Fashion Buyers
12. Denim, Streetwear & Urban Fashion Buyers
13. Accessories, Handbags & Footwear Buyers
14. Swimwear, Lingerie & Intimate Apparel Buyers
15. Sustainable Fashion & Ethical Buyers
16. Media, Publishing & Brand Partnerships
17. International Buying Offices & Sourcing Agents
18. Digital Fashion, NFT & Metaverse Buyers
19. Film, TV, Theatre & Costume Design Buyers
20. Fashion Schools & Institutional Buyers

## License / usage note

Compiled May 2026 for personal professional use. Verify contact details before outreach — companies restructure, careers pages move, and buyer contacts change.

---

Built by MisoPretty Studios.
