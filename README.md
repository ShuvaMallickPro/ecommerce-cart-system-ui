# E-commerce Cart UI (Vue 3 + Pinia)

A lightweight e-commerce UI that demonstrates **add to cart**, **quantity controls**, and **reactive totals** using **Vue 3** and **Pinia**.

- **Live demo**: [product-addtocart-statemanagement-vue.netlify.app](https://product-addtocart-statemanagement-vue.netlify.app/)
- **Repository**: [github.com/ShuvaMallickPro/ecommerce-cart-system-ui](https://github.com/ShuvaMallickPro/ecommerce-cart-system-ui)

## Features

- **Cart management**: Add/remove items and update quantities
- **State management**: Centralized store with Pinia
- **Auto calculation**: Totals update instantly as the cart changes
- **Pagination**: Browse product listings efficiently
- **Responsive UI**: Works across desktop/tablet/mobile

## Tech stack

- **Vue**: 3.x
- **State management**: Pinia
- **Build tool**: Vite
- **Styling**: Tailwind CSS

## Getting started (step-by-step)

### 1) Prerequisites

- **Node.js**: Recommended \(LTS version\)
- **npm**: Comes with Node.js

### 2) Install dependencies

```sh
npm install
```

### 3) Run the project locally (development)

```sh
npm run dev
```

Vite will print a local URL (usually `http://localhost:5173`)—open it in your browser.

### 4) Build for production

```sh
npm run build
```

### 5) Preview the production build locally

```sh
npm run preview
```

## Available scripts

- **`npm run dev`**: Start the dev server
- **`npm run build`**: Build for production
- **`npm run preview`**: Preview the production build locally

## Project notes

- **Products data**: `src/data/products.js`
- **Vite config reference**: [vitejs.dev/config](https://vitejs.dev/config/)
