# Ishara — Salla custom code

Custom sections for an electronics store on Salla (Raed theme), plus a demo product catalog.

**Live preview:** `index.html` (served by GitHub Pages). It runs the same custom code with a stand-in for the Salla SDK and 30 sample products. Prices are approximate and "add to cart" is a demo.

## Files

| Path | What it is |
|---|---|
| `salla-custom-code/ishara-custom.css` | Paste into Salla → تصميم المتجر → الكود المخصّص → CSS |
| `salla-custom-code/ishara-custom.js` | Paste into the JavaScript box. Edit `CONFIG` and `BASICS` at the top |
| `salla-custom-code/ishara-tampermonkey.user.js` | Same code as one Tampermonkey script, to preview on the store before a domain is linked |
| `products/ishara-salla-products.xlsx` | 30 products in Salla's own import template (products sheet only) |
| `products/ishara-electronics-products.csv` | Same products as CSV |
| `products/ishara-product-photos.zip` | Product photos (1200×1200, named by SKU) |

## Before importing products

Create these categories in Salla first, spelled exactly: جوالات، لابتوبات، تابلت، سماعات، ساعات ذكية، ألعاب، إكسسوارات.
Brands are left empty in the import file; add them in Salla (with logos) and assign later.

## Photo credits

Product photos are from [Unsplash](https://unsplash.com) under the Unsplash License (free for commercial use). They show the product type, not always the exact model or color. Replace them with official photos from your supplier before selling.
