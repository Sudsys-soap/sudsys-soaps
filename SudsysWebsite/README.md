# Sudsy’s Soaps storefront recreation

Portable, buildless HTML/CSS/JavaScript storefront. `dist/` is the complete static site and can be deployed to Cloudflare Pages with no build command. Serve `dist/` over HTTP for local development. The catalogue was imported from the supplied Shopify CSV export on 24 October 2026; stock is a snapshot.

## Included
- Original peach colour, circular supplied logo, responsive product grid and local product images.
- Active product catalogue, all-products listing, search and price sorting.
- Product descriptions, galleries, variant selection, quantity controls, sold-out handling.
- Browser-local basket with subtotal and stock limits.
- Existing `/products/<handle>` paths retained. Two unlisted products are omitted from listings but remain accessible by their direct paths.

## Before trading
This is a design preview. It has no payment processing, live inventory synchronization, order creation, customer accounts, gift-card issuing/redemption, tax calculation, or shipping calculation. Gift-card purchase and checkout are disabled. Add a server-side commerce implementation before enabling sales. Do not trust client-side prices or stock for real transactions. Add reviewed shop policies, business contact information and any required consent controls before launch. Cloudflare Pages SPA fallback serves product paths; other static hosts need equivalent fallback to index.html.

## Files
- `dist/catalog.json`: imported product data and snapshot inventory.
- `dist/assets/`: copied product photography and provided logo.
- `dist/app.js`: page routing and preview interactions.
- `dist/style.css`: responsive storefront styles.

No Shopify API calls, remote image URLs or Shopify subscription are required by the preview. No external JS dependencies or build tools required. Source repository hosting, custom domain and commerce integration can be configured next.
