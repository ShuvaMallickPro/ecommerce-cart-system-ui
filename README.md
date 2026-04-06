# eCommerce Cart System UI (Vue + Vite)

A lightweight, responsive e-commerce UI built with Vue and Vite. It includes product listing with pagination and a reactive cart (add/remove/update quantity) with automatic totals.

## Links

- **Live demo**: [ecommerce-product-add-to-cart-vuejs.netlify.app](https://ecommerce-product-add-to-cart-vuejs.netlify.app/)
- **Repository**: [github.com/ShuvaMallickPro/ecommerce-cart-system-ui](https://github.com/ShuvaMallickPro/ecommerce-cart-system-ui)

## Features

- **Cart management**: add/remove items, update quantities with reactive UI
- **Pagination**: browse product listings smoothly
- **Auto calculation**: totals update automatically when the cart changes
- **Responsive UI**: works well on mobile, tablet, and desktop

## Edit product image URLs

Product data is stored in `src/data/products.js`. Each item has an `image` field.

### Option A: Use any external image URL (fastest)

Update the `image` value directly:

```js
image: "https://example.com/my-product-image.jpg";
```

### Option B: Use local images (recommended for reliability)

1. Put images in `src/assets/products/` (example: `src/assets/products/p1.png`).
2. Update `image` in `src/data/products.js` using Vite’s asset URL helper:

```js
image: new URL("../assets/products/p1.png", import.meta.url).href;
```

This avoids broken external links and ensures images work in both development and production builds.

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
