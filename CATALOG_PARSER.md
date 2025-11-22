# Catalog Parser & Training Data Helper

This utility crawls a product catalog, extracts structured data (SKU, pricing, sizing, descriptions, images, etc.), and optionally emits prompt/completion pairs that can be uploaded to GoHighLevel's chatbot training interface.

## 1. Install dependencies

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## 2. Run the crawler

```bash
python catalog_parser.py "https://example.com/products" products.jsonl \
  --examples training_examples.jsonl \
  --keywords product shop collection \
  --max-pages 250 --max-products 120 --delay 0.5
```

Arguments:

- `base_url` – homepage or collection page to start from.
- `output` – JSONL file with structured product records.
- `--examples` – optional JSONL prompt/completion file aligned with GoHighLevel's importer.
- `--keywords` – words that flag URLs as likely product detail pages (defaults work for most catalogs, but you can pass things like `leggings glam-collection`).
- `--max-pages` / `--max-products` – safety caps so you can iterate quickly while testing.
- `--delay` – polite crawl delay if the storefront rate-limits.

Each `products.jsonl` entry looks like:

```json
{
  "title": "Compression Legging",
  "sku": "ABC-123",
  "price": "129",
  "description": "Graduated compression legging for lymphatic support...",
  "sizes": ["XS", "S", "M", "L"],
  "url": "https://example.com/products/compression-legging",
  "images": ["https://.../front.jpg"],
  "breadcrumbs": ["Shop", "Leggings"],
  "source_links": ["Add to bag -> https://..." ]
}
```

The optional `training_examples.jsonl` mirrors GoHighLevel's "Prompt" / "Response" schema so you can upload facts about each product directly into a chatbot's knowledge base.

## 3. Feed GoHighLevel

1. Open your GoHighLevel location → `Automation` → `Chatbots` → `Training Data`.
2. Drag the `training_examples.jsonl` file into the importer (or copy/paste rows).
3. If you only need raw facts, use `products.jsonl` as source material when crafting manual snippets.

## Notes

- The parser inspects normal HTML, schema.org Product JSON-LD, and Shopify-style option widgets, so it usually captures SKU/price/size data without extra configuration.
- You can rerun the script anytime; it overwrites the output file, so keep dated copies if you need historical snapshots.
- Typical medium catalog (≈100 products) finishes in 1–2 minutes. Large catalogs may need higher `--max-pages` and a small `--delay` to stay friendly.
