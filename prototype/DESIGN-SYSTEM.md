# Maju POS — Design System (Professional Glassmorphism, Navy & Blue)

## Product context
Maju POS is a point-of-sale web app for Indonesian UMKM (small/medium businesses: cafés, retail shops, minimarkets). UI language: Bahasa Indonesia. Currency: Rupiah (Rp 25.000 format, dot thousands separator).
Primary users: shop owners (overview, reports, settings) and cashiers (fast checkout, shifts).

Key pages & navigation (sidebar on desktop, bottom nav on mobile):
- Beranda / Dashboard — today's sales, transactions, top products, payment method split
- Kasir (POS) — product grid + category filter + cart panel + checkout (Tunai, QRIS, Debit/Transfer)
- Produk (Manajemen Produk) — product table, add/edit, categories, pricing
- Inventori — stock levels, low-stock alerts, stock in/out history
- Riwayat Transaksi — transaction list, filters, detail, refund
- Laporan — sales reports, charts, export
- Pelanggan / Member — customer list, loyalty points, purchase history
- Staf & Shift — staff accounts, roles, shift open/close with cash reconciliation
- Struk — receipt preview/print layout
- Pengaturan — store profile, payment methods, tax/service, printer, users

## Visual direction: professional glassmorphism
Glass is used for structure, not decoration. It must read as a calm, trustworthy business tool, NOT a flashy crypto/neon landing page.

- **Background canvas**: soft light gradient `bg-gradient-to-br from-slate-100 via-blue-50 to-white`, with 3 large, very blurred blue/sky blobs fixed behind content (blue-400/25, sky-300/30, blue-200/30, `blur-3xl`; never violet/purple). No busy patterns, no images behind content.
- **Glass surfaces (cards, panels, sidebar, top bar, modals)**: `bg-white/35 backdrop-blur-2xl border border-white/60 shadow-[0_8px_32px_rgba(15,23,42,0.06)] rounded-2xl`. Sidebar and top bar: `bg-white/30 backdrop-blur-2xl border-white/50`.
- **Nested / secondary glass** (inputs, table header, chips, inner tiles): `bg-white/30`–`bg-white/45` with `border-white/60`.
- **Readability rule**: all body text sits on frosted surfaces (≥ 30% white + `backdrop-blur-2xl`). Data tables use `bg-white/45` so numbers stay crisp. Never put text directly on the gradient background.
- **Dark accent surface** (sparingly, e.g. a primary KPI card or the checkout total): navy glass `bg-[#0F1E3D]/80 backdrop-blur-2xl text-white ring-1 ring-white/10`.

## Colors (Navy & Blue)
- Primary: blue-600 (#2563EB), hover blue-700 (#1D4ED8), tint blue-50/100, ring blue-500/20
- Navy: #0F1E3D — logo mark, plan card, toasts, dark KPI surfaces
- Neutrals: slate-900 headings, slate-600 body, slate-500/400 muted, slate-200 borders
- Success: emerald-600 / emerald-50 · Warning: amber-600 / amber-50 · Danger: rose-600 / rose-50 · Info: sky-600 / sky-50
- No neon, no indigo/violet/purple, no rainbow. Gradients only on the page background and, subtly, on the primary CTA (`from-blue-600 to-blue-500`).

## Typography
- Font: **Plus Jakarta Sans** only (300–700). No other fonts.
- Page title 24px/700 slate-900; section title 16px/600; body 14px/400–500; captions 12px slate-500; KPI numbers 24–30px/700 with `tabular-nums`.

## Components
- Buttons: primary = blue-600 solid (or subtle blue gradient), white text, `rounded-xl h-10 px-4 font-semibold shadow-sm shadow-blue-600/20`; secondary = glass `bg-white/60 border-white/70 text-slate-700`; destructive = rose-600.
- Inputs/selects: `bg-white/60 backdrop-blur border border-slate-200/70 rounded-xl h-10 focus:ring-4 focus:ring-blue-500/20 focus:border-blue-400`.
- Badges/status pills: tinted `bg-emerald-50/80 text-emerald-700 ring-1 ring-emerald-600/10 rounded-full text-xs font-semibold`.
- Tables: glass container, header `bg-slate-50/70 text-xs uppercase tracking-wide text-slate-500`, rows divided by `divide-slate-200/60`, row hover `bg-white/60`.
- Icons: Iconify (Lucide set, `lucide:*`), 18–20px, stroke style, slate-500 default, blue-600 active.
- Sidebar nav: active item `bg-white/80 text-blue-600 shadow-sm ring-1 ring-white` with blue left indicator; inactive slate-600, hover `bg-white/40`.
- Charts: blue-500 primary series, sky-400 secondary, emerald for positive, light slate gridlines.
- Radius: 16px (cards), 12px (controls), 9999px (pills). Spacing: 4px grid, card padding 20–24px, page gutters 24–32px.

## Motion
- Subtle only: 150–200ms ease-out on hover (slight lift `-translate-y-0.5`, shadow increase), fade/scale-in for modals. No parallax, no animated blobs.

## Constraints
- Use ONLY the fonts, colors, spacing, and component styles defined here.
- Keep all existing page content, data, labels (Bahasa Indonesia), and information architecture; glass is a visual-layer change.
- Logo: keep the existing "Maju POS" wordmark treatment as currently designed (no brand logo asset exists).
