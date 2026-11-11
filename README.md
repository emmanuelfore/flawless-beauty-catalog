# Flawless Beauty — WhatsApp / Meta product catalog

Ready-to-upload product catalog for WhatsApp (via Meta Commerce Manager), with all product photos hosted in this repository.

## Files

| File | Use |
|---|---|
| `whatsapp_catalog_all.csv` | All 27 products (recommended single upload) |
| `whatsapp_catalog_main.csv` | The 11 main wigs (WIG-001 … WIG-011) |
| `whatsapp_catalog_showroom.csv` | The 16 showroom/review wigs (SHW-001 … SHW-016) |
| `image_mapping.csv` | Shows which original WhatsApp photo became which product image |
| `wigs/` | 1080 × 1080 JPEG catalog images |

## How to upload

1. Go to [Meta Commerce Manager](https://business.facebook.com/commerce) → select/create a catalog.
2. **Catalog → Data sources → Add products → Upload file** and choose `whatsapp_catalog_all.csv`.
3. Wait for processing, then check **Diagnostics** and fix anything flagged (usually price/availability wording).
4. Connect the catalog to WhatsApp: in the WhatsApp Business app go to **Settings → Business tools → Catalog**, or connect it to your WhatsApp Business Account in Meta Business Suite.
5. WhatsApp shows the catalogue to customers; the **View** button opens a chat with the product name pre-filled.

> Telegram-style direct CSV import does not exist in the WhatsApp Business app: the CSV is imported through Meta Commerce Manager, and the catalog then syncs to WhatsApp.

## Image URLs

All `image_link` / `additional_image_link` values point to `raw.githubusercontent.com/emmanuelfore/flawless-beauty-catalog/main/wigs/…`.
The images are 1080 × 1080 JPEGs with a blurred background pad, so WhatsApp/Meta square crops do not cut off the hair length.
If you rename the repository or branch, regenerate the CSV URLs.

Verified response headers: `HTTP 200`, `content-type: image/jpeg`, no redirect, 130–235 KB per file.

## Meta requirements check

| Requirement (official Meta spec) | This catalog |
|---|---|
| `id`, `title`, `description`, `availability`, `condition`, `price`, `link`, `image_link` required | All present |
| At least one of `brand`, `gtin`, `mpn` | `brand` = Flawless Beauty |
| `google_product_category` or `fb_product_category` | Google category 181 — Wigs |
| JPEG or PNG, min 500 × 500 px, max 8 MB | JPEG, 1080 × 1080, ~130–235 KB |
| Price format `number ISO-code` | `55.00 USD` |
| `additional_image_link` quoted, comma-separated | Yes |

`link` is **required** by Meta: omitting it can stop items from uploading. It currently points to a product-specific `wa.me` link.
Meta's wording prefers a product page on your own website domain; if Diagnostics complains about the `wa.me` domain, switch `link` to a real product page.

## Products

| ID | Title | Colour | Photos |
|---|---|---|---|
| WIG-001 | Ash Blonde Ombre Dark Root Wavy Lace Front Wig | Blonde | 2 |
| WIG-002 | Burgundy Wavy Lace Front Wig | Burgundy | 3 |
| WIG-003 | 613 Blonde Wavy Lace Front Wig | Blonde | 2 |
| WIG-004 | Copper Brown Lace Front Wig | Brown | 1 |
| WIG-005 | Blonde Ginger Black Ombre Lace Front Wig | Multicolor | 2 |
| WIG-006 | Dark Brown Wavy Lace Front Wig | Brown | 1 |
| WIG-007 | Plum Purple Wavy Lace Front Wig | Purple | 2 |
| WIG-008 | Burgundy Short Bob Wig | Burgundy | 6 |
| WIG-009 | Honey Blonde Short Bob Wig | Blonde | 8 |
| WIG-010 | Brown Ombre Ash Highlight Wavy Lace Front Wig | Brown | 2 |
| WIG-011 | Dark Auburn Long Wavy Lace Front Wig | Red | 1 |
| SHW-001 | Chestnut Brown Body Wave Lace Front Wig | Brown | 3 |
| SHW-002 | Brown Honey Highlight Body Wave Lace Front Wig | Brown | 2 |
| SHW-003 | 613 Blonde Body Wave Lace Front Wig | Blonde | 2 |
| SHW-004 | Burgundy Body Wave Lace Front Wig | Burgundy | 2 |
| SHW-005 | Ginger Copper Body Wave Lace Front Wig | Orange | 2 |
| SHW-006 | Dark Brown Caramel Highlight Wavy Lace Front Wig | Brown | 2 |
| SHW-007 | Black Body Wave Lace Front Wig | Black | 1 |
| SHW-008 | Honey Brown Highlighted Long Straight Lace Front Wig | Brown | 1 |
| SHW-009 | Ombre Ash Blonde Straight Lace Front Wig | Blonde | 1 |
| SHW-010 | Ash Blonde Layered Lace Front Wig | Blonde | 1 |
| SHW-011 | 613 Blonde Long Straight Lace Front Wig | Blonde | 1 |
| SHW-012 | Auburn Brown Body Wave Wig | Brown | 1 |
| SHW-013 | Chocolate Brown Straight Lace Front Wig | Brown | 1 |
| SHW-014 | Black Body Wave Headband Wig | Black | 1 |
| SHW-015 | Highlighted Wavy Wig | Brown | 1 |
| SHW-016 | Highlighted Bob Lace Front Wig | Brown | 2 |

Prices are set at **55.00 USD** and condition **new**, matching the source catalog. Edit the CSV if that changes.
