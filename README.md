# Ishara — Salla custom code

Custom sections for an electronics store on Salla (Raed theme), plus a demo product catalog.

**Live preview:** a full demo store that runs the same custom code with a stand-in for the Salla SDK and 30 sample products. Prices are approximate; orders are a demo (no payment, nothing is sent; cart, wishlist and orders stay in the browser).

| Page | What it shows |
|---|---|
| `index.html` | Home: all custom sections (hero, flash sale, setup builder, quiz, compare, categories, offers…) |
| `collection.html#c1` … `#c7`, `#offers`, `#all` | Category page in two layouts (showroom and banner), filters, sorting, quick view, compare |
| `product.html#p7001` … `#p7030` | Product page: buy box, specs, and the custom bundle, installments, trade-in and FAQ sections |
| `cart.html` | Cart with quantities, coupon (`ISHARA10`), free-shipping meter |
| `checkout.html` | Checkout: contact, address, shipping and payment choice, order confirmation |
| `account.html`, `wishlist.html`, `info.html` | Orders with tracking, wishlist, store policies and contact |

The preview shell lives in `assets/` (`shop.css`, `shop.js`, `products.js`) and `img/`. Only `salla-custom-code/` goes into Salla.

## Files

| Path | What it is |
|---|---|
| `salla-custom-code/ishara-custom.css` | Paste into Salla → تصميم المتجر → الكود المخصّص → CSS |
| `salla-custom-code/ishara-custom.js` | Paste into the JavaScript box. Edit `CONFIG` and `BASICS` at the top |
| `salla-custom-code/ishara-tampermonkey.user.js` | Same code as one Tampermonkey script, to preview on the store before a domain is linked |
| `products/ishara-salla-products.xlsx` | 30 products in Salla's own import template (products sheet only) |
| `products/ishara-electronics-products.csv` | Same products as CSV |
| `products/ishara-product-photos.zip` | Product photos (1200×1200, named by SKU) |

## Shopping helpers

`CONFIG.shopping` in the JS adds store-wide interactions on top of Raed:
free-shipping progress bar on the cart page (set `threshold` to match your Salla shipping rule),
a sticky buy bar on product pages that presses the theme's own add-to-cart button,
recently viewed products, wishlist hearts on the custom sections' cards, and a back-to-top button.

## Category page

The category page (`product.index`) comes in two layouts. Pick one in `CONFIG.collection.layout`, or set a different layout for some categories in `CONFIG.collection.layouts` (by category id, for example `{ 123456: 'showroom' }`).

- **`banner`** (default): a dark banner with the category name, live stats (product count, lowest price, how many are on sale), a few product photos, and quick links to the other categories.
- **`showroom`**: a light editorial header with a large title and a stats strip, the categories as underlined tabs, "مختارات القسم" (the product with the biggest discount, the cheapest one and a newer one, each with add to cart and a wishlist heart), a grid / list switch above the theme's product list, softer product cards, and photo tiles linking to the other categories at the end of the page.

Both layouts only add sections around the theme's own product list. Raed's filters, sorting, paging and product links keep working. The list view is remembered in the visitor's browser. In the preview, each category has its own layout: laptops (لابتوبات) use the banner layout, and phones (جوالات) and the other categories use the showroom layout.

## Before importing products

Create these categories in Salla first, spelled exactly: جوالات، لابتوبات، تابلت، سماعات، ساعات ذكية، ألعاب، إكسسوارات.
Brands are left empty in the import file; add them in Salla (with logos) and assign later.

## Photo credits

Product photos are from [Unsplash](https://unsplash.com) under the Unsplash License (free for commercial use). They show the product type, not always the exact model or color. Replace them with official photos from your supplier before selling.
