# ElectroElite — Premium Home Appliance Store

> **Tagline:** Upgrade Your Home. Upgrade Your Life.

A high-end, fully responsive Next.js 16 e-commerce storefront for premium home & electrical appliances. Built with TypeScript, Tailwind CSS 4, shadcn/ui, Zustand, and Embla Carousel.

![ElectroElite](https://img.shields.io/badge/Next.js-16-black) ![TypeScript](https://img.shields.io/badge/TypeScript-5-blue) ![Tailwind](https://img.shields.io/badge/Tailwind-4-38bdf8) ![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 🧭 **Mega-menu header** with category dropdowns, prominent search, and live cart/compare counters
- 🎞️ **Hero slider** showcasing 4K OLED TVs, Smart Inverter ACs, Refrigerators, and Solar Inverters
- 🗂️ **Featured Categories** bento grid (Entertainment, Cooling, Kitchen, Power, Heating)
- 🛒 **Product catalog** with 26 realistic products across all categories
- 🎚️ **Filter sidebar** — filter by Brand, Price, Energy Rating, and Capacity
- ⚖️ **Compare feature** — compare up to 4 products side-by-side with spec table
- 🔥 **Trending Now** section featuring best-selling Inverters & Pedestal Fans
- 💳 **Cart drawer** with quantity steppers, EMI breakdown, free-delivery progress
- 📰 **Footer** with newsletter signup, ZIP-code store locator, and contact details
- 📱 **Fully responsive** — tested at 390px (iPhone 14) and 1440px viewports
- 💾 **Persisted state** — cart and compare list saved to localStorage

## 🎨 Design System

| Token | Value |
|-------|-------|
| Primary Navy | `#0F1E3D` |
| Navy Light | `#1E3A6B` |
| Slate Gray | slate-* palette |
| Accent Gold | `#F59E0B` |
| Background | `#FFFFFF` |
| Body Font | Inter |
| Display Font | Plus Jakarta Sans |

## 🛠️ Tech Stack

- **Framework:** Next.js 16 (App Router, Turbopack)
- **Language:** TypeScript 5
- **Styling:** Tailwind CSS 4 + shadcn/ui (New York style)
- **State Management:** Zustand (with persist middleware)
- **Carousel:** Embla Carousel React
- **Icons:** Lucide React
- **Toasts:** Sonner
- **ORM:** Prisma (configured, optional — uses static catalog by default)

## 🚀 Quick Start

### Prerequisites

- Node.js 18.18+ or 20+
- npm, pnpm, or bun

### Installation

```bash
# 1. Unzip the project
unzip electroelite-source.zip
cd electroelite-source

# 2. Install dependencies
npm install
# or
pnpm install
# or
bun install

# 3. Run the dev server
npm run dev
# or
bun run dev

# 4. Open http://localhost:3000
```

### Build for Production

```bash
npm run build
npm run start
```

## 📂 Project Structure

```
.
├── src/
│   ├── app/
│   │   ├── globals.css         # Navy/slate/white theme + animations
│   │   ├── layout.tsx          # Inter + Plus Jakarta fonts + metadata
│   │   └── page.tsx            # Main page composition
│   ├── components/
│   │   ├── site/               # ElectroElite-specific components
│   │   │   ├── header.tsx              # Sticky header with mega-menu
│   │   │   ├── hero-slider.tsx         # 4-slide auto-playing carousel
│   │   │   ├── featured-categories.tsx # Bento category grid
│   │   │   ├── product-card.tsx        # Product card with all features
│   │   │   ├── product-catalog.tsx     # Catalog + filter sidebar
│   │   │   ├── trending-now.tsx        # Trending section
│   │   │   ├── value-props.tsx         # Value props + newsletter CTA
│   │   │   ├── footer.tsx              # Footer with store locator
│   │   │   ├── cart-drawer.tsx         # Cart Sheet
│   │   │   └── compare-drawer.tsx      # Compare Sheet with table
│   │   └── ui/                 # shadcn/ui components
│   ├── lib/
│   │   ├── catalog.ts          # Product data + categories + brands
│   │   ├── store.ts            # Zustand store (cart/compare/wishlist/search)
│   │   ├── db.ts               # Prisma client
│   │   └── utils.ts            # Tailwind class merge helper
│   └── hooks/                  # React hooks (use-mobile, use-toast)
├── prisma/
│   └── schema.prisma           # Database schema
├── public/                     # Static assets
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── postcss.config.mjs
├── next.config.ts
├── eslint.config.mjs
└── README.md
```

## 🌐 Deploy to Vercel

This is a standard Next.js 16 app — deployment to Vercel is straightforward.

### Option A: Dashboard Upload (Fastest)

1. Push this folder to a GitHub repo (see "Push to GitHub" below)
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import your GitHub repo
4. Vercel auto-detects Next.js — keep these defaults:
   - **Framework Preset:** Next.js
   - **Build Command:** `next build` (default)
   - **Output Directory:** `.next` (default, auto-detected)
   - **Root Directory:** `./` (leave as default — `package.json` is at root)
5. Click **Deploy** — done in ~2 minutes! 🎉

### Option B: Vercel CLI

```bash
npm i -g vercel
vercel          # Deploy preview
vercel --prod   # Deploy production
```

### Vercel Settings Checklist

If Vercel fails to build, check:

| Setting | Value |
|---------|-------|
| Framework Preset | Next.js |
| Root Directory | `./` (Not Defined — package.json is at root) |
| Build Command | `next build` (default) |
| Output Directory | `.next` (auto-detected) |
| Install Command | `npm install` (default) |
| Node.js Version | 20.x (recommended) |

### No `vercel.json` needed!

This is a single-page app with no client-side routing, so you do **not** need the `vercel.json` rewrite rules you might have seen in other tutorials. Just deploy as-is.

## 📤 Push to GitHub

```bash
# 1. Initialize git (if not done)
git init
git add .
git commit -m "Initial commit: ElectroElite home appliance store"

# 2. Create a new repo on github.com (don't add README/license there)

# 3. Add remote and push
git remote add origin https://github.com/YOUR_USERNAME/electroelite.git
git branch -M main
git push -u origin main
```

Or use the GitHub Desktop app: drag the unzipped folder into GitHub Desktop and click "Publish repository".

## 🎯 Product Catalog

26 products across 5+ categories:

- **Entertainment:** Neo QLED 8K TV, OLED evo C4, BRAVIA XR A95L, Samsung & LG Soundbars
- **Cooling:** WindFree Inverter AC, LG Dual Inverter AC, Voltas Window AC, BLDC Ceiling Fan, Pedestal Fan, Exhaust Fan
- **Kitchen:** Side-by-Side Refrigerator, Double-door Fridge, Mini Fridge, Convection Microwave, OTG, Dishwasher
- **Power:** Luminous Zelio+ Inverter, Microtek Solar Hybrid Inverter, Solar Battery, UPS Stabilizer
- **Heating:** Oil-Filled Radiator, Water Heater, Gas Furnace
- **Bonus:** Front Load Washer, HEPA Air Purifier

To add or edit products, modify `src/lib/catalog.ts`.

## 🧪 Verification

- ✅ ESLint passes clean (0 errors, 0 warnings)
- ✅ Tested at mobile (390px) and desktop (1440px) viewports
- ✅ All interactive flows verified: search, filter, sort, add-to-cart, compare, category navigation, store locator

## 📝 License

MIT — feel free to use this as a starting point for your own e-commerce projects.

## 💡 Suggested Next Steps

- Swap emoji product images for real product photos (drop them in `public/products/` and update the `image` field in `src/lib/catalog.ts`)
- Wire up real checkout with Stripe
- Add a Prisma-backed product database (already configured)
- Add product detail pages with `/[id]` route
- Add user authentication with NextAuth.js (already installed)

---

Built with ❤️ for premium homes.
