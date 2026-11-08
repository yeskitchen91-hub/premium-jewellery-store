# HeerOra — Premium Jewellery Storefront

HeerOra is an owner-made artificial jewellery brand. This repository contains a lightweight, responsive storefront preview for a mix of trendy, traditional and occasion styles.

> **Demo status:** Product names, descriptions, prices and imagery are temporary mockups. Confirm and replace them before selling. Payment, WhatsApp, shipping, customer support and return policies are not configured.

## Technologies

- HTML5
- CSS3 with responsive layouts and CSS variables
- Vanilla JavaScript
- Google Fonts (loaded from Google Fonts when online)
- LocalStorage for this browser's cart and wishlist

No framework, package manager or build step is required.

## Features

- Homepage, shop, product details, cart, checkout preview, wishlist, About, Contact, FAQ and pending policies pages
- Product search, category and price filters, and sorting
- Product detail URLs such as `product.html?id=1`
- Cart quantity controls, subtotal calculation and browser persistence
- Wishlist add/remove and browser persistence
- Mobile layout and keyboard focus styles
- Checkout form validation in a non-submitting preview

## Project structure

```text
jewellery-store/
├── index.html
├── shop.html
├── product.html
├── cart.html
├── checkout.html
├── about.html
├── contact.html
├── wishlist.html
├── faq.html
├── policies.html
├── css/style.css
├── js/
│   ├── main.js
│   ├── products.js
│   ├── cart.js
│   ├── wishlist.js
│   └── checkout.js
├── images/
│   ├── logo/heerora-logo-reference.jpg
│   └── banners/heerora-campaign-mockup.png
├── favicon/favicon.svg
├── PROJECT_BRIEF.md
├── .gitignore
└── README.md
```

## Preview locally

1. Open the `jewellery-store` folder.
2. Double-click `index.html` to open the homepage in your browser.
3. Use the navigation to explore the shop, add demo items to the bag, and save wishlist items.

A local static server can also serve this folder if you prefer. No build or install command is required.

## Update products and prices

Open `js/products.js` in a text editor. Each item is an object in the `products` array. Update its unique `id`, `name`, `category`, `price`, `description`, `material`, `color`, `images`, `featured`, `isNew`, `stock` and `care` fields. Prices are in Indian rupees. Use `stock: null` only while the real quantity is unknown; set a confirmed quantity before launch.

The eight current products are examples only. Replace their names, prices and descriptions with confirmed catalogue details.

## Replace product images

1. Add accurate product photos under `images/products/` (WebP or appropriately sized JPEG/PNG is suitable).
2. In `js/products.js`, update each product's `images` array to the new relative path, for example `images/products/earrings-01.webp`.
3. Keep product photos proportional and use descriptive alt text; the product card and detail view already label the current imagery as mockup content.

The current sample product image references the generated campaign mockup at `images/banners/heerora-campaign-mockup.png`.

## Update the logo and visual style

Replace `images/logo/heerora-logo-reference.jpg` with the approved final logo, retaining the path or updating the logo reference in `js/main.js`. Change the provisional colour variables near the top of `css/style.css` after the final palette is approved.

## WhatsApp and contact information

No WhatsApp number or contact channel has been supplied. Do not publish a made-up number. Add the confirmed contact channel in the footer in `js/main.js` and configure a WhatsApp link only after HeerOra provides its correct business number. No order messages are currently transmitted.

## Payments and checkout status

There is no live UPI, Cash on Delivery or payment gateway connection. The checkout is only a local preview: it does not submit orders, send entered details or process payments. The cart and wishlist are saved only in the current browser and are not shared with the business. A live payment integration needs a secure backend or trusted ecommerce/payment service for order creation and payment verification. Never put gateway secret keys in frontend files.

Before launch, confirm product facts, payment setup, shipping coverage and charges, delivery estimates, return/exchange/refund terms, privacy notice, and support details.

## Upload to GitHub

After creating an empty GitHub repository, connect this local project folder and push its first commit:

```bash
git remote add origin https://github.com/YOUR-USERNAME/premium-jewellery-store.git
git branch -M main
git push -u origin main
```

Replace `YOUR-USERNAME` with the GitHub account name and use the repository URL GitHub shows. Do not add credentials or customer information to the project.

## Future static deployment and domain

This repository is structured for a static host such as GitHub Pages. GitHub Pages can be enabled later from the repository's **Settings → Pages** after the upload; no deployment has been configured here. The site does not require a domain to work on a host's provided URL.

A custom domain can be considered later, after it is purchased. Domain connection would require adding the domain in the host's settings and then setting the DNS records supplied by that host. No domain is included or hardcoded in this project.
