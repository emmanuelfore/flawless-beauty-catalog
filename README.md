# Flawless Beauty — WhatsApp / Meta product catalog

Ready-to-upload product catalog for WhatsApp (via Meta Commerce Manager), with all product photos hosted in this repository.

## Files

| File | Use |
|---|---|
| `whatsapp_catalog_all.csv` | All 78 products (recommended single upload) |
| `whatsapp_catalog_main.csv` | Original 11 main wigs (WIG-001 … WIG-011) |
| `whatsapp_catalog_showroom.csv` | Original 16 showroom wigs (SHW-001 … SHW-016) |
| `whatsapp_catalog_new.csv` | 51 new wigs from the price-named zips (WIG-012 … WIG-062) |
| `image_mapping.csv` | Which original WhatsApp photo became which product image |
| `wigs/` | 1080 × 1080 JPEG catalog images |

## Price groups

The new zips were named by price. `10.zip`, `15.zip`, `18.zip` / `18_2.zip`, `20.zip`, `25.zip` / `25_2.zip`, `35.zip` / `35_2.zip` became products priced **10, 15, 18, 20, 25 and 35 USD** respectively. A suffix such as `_2` indicates a second batch at the same price.

Each visually distinct wig in a zip became its own product; multiple photos of the same wig are grouped as `additional_image_link`. Composite colour-range photos became "Assorted Colours" listings.

## How to upload

1. Go to [Meta Commerce Manager](https://business.facebook.com/commerce) → select/create a catalog.
2. **Catalog → Data sources → Add products → Upload file** and choose `whatsapp_catalog_all.csv`.
3. Wait for processing, then check **Diagnostics** and fix anything flagged.
4. Connect the catalog to WhatsApp: in the WhatsApp Business app go to **Settings → Business tools → Catalog**, or connect it to your WhatsApp Business Account in Meta Business Suite.
5. WhatsApp shows the catalogue to customers; the **View** button opens a chat with the product name pre-filled.

> Telegram-style direct CSV import does not exist in the WhatsApp Business app: the CSV is imported through Meta Commerce Manager, and the catalog then syncs to WhatsApp.

## Image URLs

All `image_link` / `additional_image_link` values point to `raw.githubusercontent.com/emmanuelfore/flawless-beauty-catalog/main/wigs/…`.
Images are 1080 × 1080 JPEGs with a blurred background pad, so WhatsApp/Meta square crops do not cut off the hair length.
If you rename the repository or branch, regenerate the CSV URLs.

## Meta requirements check

| Requirement (official Meta spec) | This catalog |
|---|---|
| `id`, `title`, `description`, `availability`, `condition`, `price`, `link`, `image_link` required | All present |
| At least one of `brand`, `gtin`, `mpn` | `brand` = Flawless Beauty |
| `google_product_category` or `fb_product_category` | Google category 181 — Wigs |
| JPEG or PNG, min 500 × 500 px, max 8 MB | JPEG, 1080 × 1080 |
| Price format `number ISO-code` | e.g. `20.00 USD` |
| `additional_image_link` quoted, comma-separated | Yes |

`link` is **required** by Meta. It currently points to a product-specific `wa.me` link. Meta prefers a product page on your own domain; if Diagnostics complains, switch `link` to a real product page.

## Products

| ID | Title | Price | Colour | Photos |
|---|---|---|---|---|
| WIG-001 | Ash Blonde Ombre Dark Root Wavy Lace Front Wig | 55.00 USD | Blonde | 2 |
| WIG-002 | Burgundy Wavy Lace Front Wig | 55.00 USD | Burgundy | 3 |
| WIG-003 | 613 Blonde Wavy Lace Front Wig | 55.00 USD | Blonde | 2 |
| WIG-004 | Copper Brown Lace Front Wig | 55.00 USD | Brown | 1 |
| WIG-005 | Blonde Ginger Black Ombre Lace Front Wig | 55.00 USD | Multicolor | 2 |
| WIG-006 | Dark Brown Wavy Lace Front Wig | 55.00 USD | Brown | 1 |
| WIG-007 | Plum Purple Wavy Lace Front Wig | 55.00 USD | Purple | 2 |
| WIG-008 | Burgundy Short Bob Wig | 55.00 USD | Burgundy | 6 |
| WIG-009 | Honey Blonde Short Bob Wig | 55.00 USD | Blonde | 8 |
| WIG-010 | Brown Ombre Ash Highlight Wavy Lace Front Wig | 55.00 USD | Brown | 2 |
| WIG-011 | Dark Auburn Long Wavy Lace Front Wig | 55.00 USD | Red | 1 |
| SHW-001 | Chestnut Brown Body Wave Lace Front Wig | 55.00 USD | Brown | 3 |
| SHW-002 | Brown Honey Highlight Body Wave Lace Front Wig | 55.00 USD | Brown | 2 |
| SHW-003 | 613 Blonde Body Wave Lace Front Wig | 55.00 USD | Blonde | 2 |
| SHW-004 | Burgundy Body Wave Lace Front Wig | 55.00 USD | Burgundy | 2 |
| SHW-005 | Ginger Copper Body Wave Lace Front Wig | 55.00 USD | Orange | 2 |
| SHW-006 | Dark Brown Caramel Highlight Wavy Lace Front Wig | 55.00 USD | Brown | 2 |
| SHW-007 | Black Body Wave Lace Front Wig | 55.00 USD | Black | 1 |
| SHW-008 | Honey Brown Highlighted Long Straight Lace Front Wig | 55.00 USD | Brown | 1 |
| SHW-009 | Ombre Ash Blonde Straight Lace Front Wig | 55.00 USD | Blonde | 1 |
| SHW-010 | Ash Blonde Layered Lace Front Wig | 55.00 USD | Blonde | 1 |
| SHW-011 | 613 Blonde Long Straight Lace Front Wig | 55.00 USD | Blonde | 1 |
| SHW-012 | Auburn Brown Body Wave Wig | 55.00 USD | Brown | 1 |
| SHW-013 | Chocolate Brown Straight Lace Front Wig | 55.00 USD | Brown | 1 |
| SHW-014 | Black Body Wave Headband Wig | 55.00 USD | Black | 1 |
| SHW-015 | Highlighted Wavy Wig | 55.00 USD | Brown | 1 |
| SHW-016 | Highlighted Bob Lace Front Wig | 55.00 USD | Brown | 2 |
| WIG-012 | Brown Long Straight Wig with Fringe | 10.00 USD | Brown | 2 |
| WIG-013 | Black Long Kinky Straight Wig | 10.00 USD | Black | 2 |
| WIG-014 | Black Afro Curly Wig | 10.00 USD | Black | 1 |
| WIG-015 | Black Curly Wig with Blonde Ends | 10.00 USD | Multicolor | 2 |
| WIG-016 | Burgundy Curly Wig | 10.00 USD | Burgundy | 2 |
| WIG-017 | Brown Short Bob Wig with Fringe | 10.00 USD | Brown | 1 |
| WIG-018 | Copper Short Bob Wig | 10.00 USD | Copper | 2 |
| WIG-019 | Dark Brown Curly Wig | 10.00 USD | Brown | 1 |
| WIG-020 | Black Pixie Cut Wig | 10.00 USD | Black | 2 |
| WIG-021 | Copper Curly Wig | 10.00 USD | Copper | 2 |
| WIG-022 | Black to Blonde Ombre Bob Wig | 15.00 USD | Multicolor | 1 |
| WIG-023 | Black to Copper Ombre Bob Wig | 15.00 USD | Multicolor | 3 |
| WIG-024 | Auburn Long Headband Wig | 18.00 USD | Brown | 1 |
| WIG-025 | Black Long Headband Wig | 18.00 USD | Black | 1 |
| WIG-026 | Brown Curly Long Wig | 18.00 USD | Brown | 2 |
| WIG-027 | Black Curly Long Wig | 18.00 USD | Black | 3 |
| WIG-028 | Black Root Honey Blonde Wavy Wig | 20.00 USD | Blonde | 2 |
| WIG-029 | Brown Root Honey Blonde Wavy Wig | 20.00 USD | Blonde | 1 |
| WIG-030 | Brown Bob Wig with Fringe | 20.00 USD | Brown | 2 |
| WIG-031 | Wine Red Wavy Wig | 20.00 USD | Red | 2 |
| WIG-032 | Bright Red Wavy Wig with Fringe | 20.00 USD | Red | 1 |
| WIG-033 | Black Wavy Wig with Fringe | 20.00 USD | Black | 1 |
| WIG-034 | Pale Blonde Wavy Wig | 20.00 USD | Blonde | 1 |
| WIG-035 | Golden Blonde Long Straight Wig | 20.00 USD | Blonde | 3 |
| WIG-036 | Black Long Straight Wig | 20.00 USD | Black | 4 |
| WIG-037 | Dark Purple Wavy Wig | 20.00 USD | Purple | 2 |
| WIG-038 | Platinum Blonde Wig with Fringe | 20.00 USD | Blonde | 2 |
| WIG-039 | Black Root Red Long Wig | 20.00 USD | Red | 2 |
| WIG-040 | Ginger Copper Long Straight Wig | 20.00 USD | Copper | 2 |
| WIG-041 | Light Brown Wavy Wig with Fringe | 20.00 USD | Brown | 1 |
| WIG-042 | Black Root Ash Blonde Wavy Wig | 20.00 USD | Blonde | 1 |
| WIG-043 | Burgundy Long Straight Wig | 20.00 USD | Burgundy | 1 |
| WIG-044 | Black Root Burgundy Wavy Wig | 20.00 USD | Burgundy | 1 |
| WIG-045 | Dark Burgundy Long Wig with Fringe | 20.00 USD | Burgundy | 1 |
| WIG-046 | Black Short Curly Bob with Caramel Highlights | 20.00 USD | Multicolor | 4 |
| WIG-047 | Black Shoulder-Length Wavy Bob | 20.00 USD | Black | 1 |
| WIG-048 | Honey Copper Short Wavy Bob | 20.00 USD | Copper | 1 |
| WIG-049 | Body Wave Wig Assorted Colours | 25.00 USD | Multicolor | 1 |
| WIG-050 | Platinum Blonde Wavy Wig | 25.00 USD | Blonde | 1 |
| WIG-051 | Black to Green Ombre Bob Wig | 25.00 USD | Multicolor | 1 |
| WIG-052 | Blonde to Blue Ombre Wig | 25.00 USD | Multicolor | 1 |
| WIG-053 | Copper Orange Long Wavy Wig | 25.00 USD | Orange | 2 |
| WIG-054 | Burgundy Curly Long Wig | 25.00 USD | Burgundy | 1 |
| WIG-055 | Auburn Brown Long Wavy Wig | 25.00 USD | Brown | 2 |
| WIG-056 | Black Silver Red Streak Wavy Wig | 25.00 USD | Multicolor | 2 |
| WIG-057 | Black Long Wavy Wig | 25.00 USD | Black | 1 |
| WIG-058 | Curly Wig Assorted Colours | 35.00 USD | Multicolor | 1 |
| WIG-059 | Burgundy Short Curly Wig | 35.00 USD | Burgundy | 2 |
| WIG-060 | Ginger Copper Short Curly Wig | 35.00 USD | Copper | 5 |
| WIG-061 | Black Short Straight Bob Wig | 35.00 USD | Black | 2 |
| WIG-062 | Black Root Blonde Ombre Bob Wig | 35.00 USD | Multicolor | 3 |
