# Abdur Rahman Razu — Photography Portfolio

A single-page photography and videography portfolio for **Abdur Rahman Razu**, a freelance photographer based in Dhaka, Bangladesh. The site showcases documentary, street, editorial, and portrait work with a photo gallery, embedded video reels, about section, and contact form.

**Live site:** [photographer-abdur-rahman-nt5b.vercel.app](https://photographer-abdur-rahman-nt5b.vercel.app)

## Features

- **Hero** — Full-screen intro with background image, headline, and calls to action
- **Photo gallery** — Filterable grid (Documentary, Editorial, Street, Portrait) with lightbox modal and keyboard navigation
- **Videography** — YouTube and Facebook reel embeds in a modal player
- **About** — Bio, stats, and portrait image
- **Contact** — Inquiry form with toast feedback, email/phone/location, and social links
- **Navigation** — Sticky header with mobile menu and CV download (“Hire Me”)
- **SEO** — Open Graph and Twitter metadata configured in the App Router layout
- **Performance** — Static generation, optimized images via `next/image`, blur placeholders, and loading skeletons

## Tech Stack

- [Next.js 16](https://nextjs.org/) (App Router, Turbopack in dev)
- [React 19](https://react.dev/)
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [shadcn/ui](https://ui.shadcn.com/) (Radix UI primitives)
- [Lucide React](https://lucide.dev/) icons
- Google Fonts: Cormorant Garamond (display) and DM Sans (body)

## Getting Started

### Prerequisites

- Node.js 18+
- npm

### Install

```sh
npm install --legacy-peer-deps
```

> **Note:** `next-themes@0.3.0` does not declare React 19 as a peer dependency, so a plain `npm install` may fail. Use `--legacy-peer-deps`, or upgrade `next-themes` to `^0.4.6` for a conflict-free install.

### Development

```sh
npm run dev
```

Opens at [http://localhost:8080](http://localhost:8080).

If you see Turbopack errors referencing an old project path after moving the repo, clear the cache and restart:

```sh
rm -rf .next
npm run dev
```

### Production

```sh
npm run build
npm run start
```

### Lint

```sh
npm run lint
```

## Project Structure

```
src/
├── app/
│   ├── layout.tsx      # Root layout, fonts, SEO metadata
│   ├── page.tsx        # Main portfolio page (single route)
│   ├── globals.css     # Tailwind base styles and theme tokens
│   ├── providers.tsx   # Tooltip and toast providers
│   └── not-found.tsx   # 404 page
├── components/
│   ├── Hero.tsx
│   ├── Gallery.tsx     # Photo grid, filters, lightbox, video modals
│   ├── About.tsx
│   ├── Contact.tsx
│   ├── Navigation.tsx
│   ├── Footer.tsx
│   ├── MediaSkeleton.tsx
│   └── ui/             # shadcn/ui components
├── data/
│   └── media.ts        # Photo and video content
├── assets/             # Source images (hero, about, gallery)
├── hooks/
└── lib/
    └── utils.ts

public/
├── og-image.jpg        # Social preview image (1200×630 recommended)
├── Abdur Rahman's cv.pdf
├── favicon.svg
├── favicon.ico
├── favicon-32x32.png
└── apple-touch-icon.png
```

## Customization

### Update portfolio content

Edit `src/data/media.ts` to change photos, videos, categories, and alt text. Add or replace image files in `src/assets/` and import them in that file.

### Update site metadata

Edit `src/app/layout.tsx` for the page title, description, keywords, Open Graph/Twitter cards, and production URL (`metadataBase`).

### Update contact details

Edit `src/components/Contact.tsx` for email, phone, location, and social links.

### Replace static files

- **CV:** Replace `public/Abdur Rahman's cv.pdf`
- **Social preview:** Replace `public/og-image.jpg` (keep 1200×630 for best results)
- **Favicons:** Replace files in `public/`

## Social Preview

Link previews use `public/og-image.jpg`, referenced in `src/app/layout.tsx` via Open Graph and Twitter metadata. When replacing the image, use **1200×630** for broad platform compatibility.

## Deployment

The site is configured for static export-friendly hosting on Vercel. Push to your connected repository or deploy the output of `npm run build`.

Production URL:

```txt
https://photographer-abdur-rahman-nt5b.vercel.app
```

Update `siteUrl` in `src/app/layout.tsx` if the domain changes.

## License

Private project. All photography © Abdur Rahman Razu.
