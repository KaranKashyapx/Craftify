# CRAFTIFY: An Artisanal Candles & Handcrafted Lifestyle E-Commerce Storefront

**Submitted by:** Karan Arvind Gond  
**Course:** B.Sc. Computer Science (SEM V, 2026–2027), University of Mumbai  
**Live GitHub Pages Showcase:** [https://karankashyapx.github.io/Craftify/](https://karankashyapx.github.io/Craftify/)

---

## Project Overview

**CRAFTIFY** is a full-stack e-commerce web application built for handcrafted candles, festive modak candles, decorative lotus flower candles, aromatic tin candles, and sustainable home decor.

### Key Engineering Highlights
1. **Responsive Dark-Amber Storefront:** Built with Next.js App Router, React, and Tailwind CSS (`#1e1912` warm dark-brown & `#f59e0b` amber aesthetic) plus a self-contained static GitHub Pages build (`index.html`, `shop.html`, `about.html`, `contact.html`).
2. **Search, Filter & Sort:** Real-time keyword search, category filtering (`All Candles`, `Festive Modak`, `Aromatic Jars`, `Decorative & Lotus`), and sorting (`Featured`, `Price Low to High`, `Price High to Low`, `Customer Rating`).
3. **Interactive Cart Drawer & Sync:** Persisted in `localStorage` (`craftify-cart`) for guests and synchronized with the MongoDB cart at sign-in (`POST /api/v1/cart/sync`).
4. **Server-Calculated Orders in Integer Paise:** Subtotal, shipping (`₹0` when subtotal `>= ₹499`, else `₹49`), and `8%` estimated GST are calculated in integer paise (`₹1 = 100 paise`) with atomic stock reservation and `CF-XXXXXXXX` order references.
5. **Role-Protected Administrator Panel:** Live sales summary (`₹8,420.00`), order status transitions (`pending` → `processing` → `shipped` → `delivered`, or `cancelled` with automatic stock restoration), and product/category CRUD.

---

## How to Push Directly to Your GitHub Repository

```bash
git init
git add .
git commit -m "Restore complete Craftify storefront and full-stack project"
git branch -M main
git remote add origin https://github.com/karankashyapx/Craftify.git
git push -u origin main --force
```

Once pushed, enable **Settings → Pages → Deploy from a branch (`main` / `/ (root)`)** and your live website will be active at `https://karankashyapx.github.io/Craftify/`.

---

## Running Full-Stack Locally

### 1. Backend (`backend/`)
```bash
cd backend
npm install
cp .env.example .env
npm run seed
npm run dev
# Run the 9 automated backend tests:
npm test
```

### 2. Frontend (`Frontend/`)
```bash
cd Frontend
npm install
npm run dev
```
