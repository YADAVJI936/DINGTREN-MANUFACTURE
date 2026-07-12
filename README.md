# Manufacturer Business Manager

A Vyapar-style billing, inventory, GST, production (BOM) and online-ordering app
prototype, built with React + Vite.

## Run it on your computer

You need [Node.js](https://nodejs.org) installed (version 18 or higher). Check with:

```bash
node -v
```

Then, inside this folder:

```bash
npm install
npm run dev
```

This will print a local address, usually `http://localhost:5173`. Open that in
your browser — the app is now running on your machine.

To build a production-ready static version (for hosting):

```bash
npm run build
```

This creates a `dist/` folder you can upload to any static host.

## Put it on GitHub

1. Create a new empty repository on GitHub (no README/license, so it stays empty).
2. In this folder, run:

```bash
git init
git add .
git commit -m "Initial commit: manufacturer business manager app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Replace `YOUR_USERNAME/YOUR_REPO_NAME` with your actual GitHub repo path.

## Put it online for free (optional)

Once it's on GitHub, the easiest free hosting options are:

- **Vercel** (vercel.com) — sign in with GitHub, click "New Project," pick this
  repo, and it deploys automatically (auto-detects Vite).
- **Netlify** (netlify.com) — same idea: connect the repo, build command
  `npm run build`, publish directory `dist`.

Either gives you a live public URL you (and customers, for the storefront view)
can open from any phone or computer.

## Admin login

- Username: `admin`
- Password: `manufacture123`

Change these in `src/App.jsx` — search for `ADMIN_USER` and `ADMIN_PASS` near the
top of the file.

## Important: data storage limitation

This version saves data using your browser's `localStorage`, which means:

- Data stays **only on the device/browser** where you use it. It will not
  automatically appear on your phone if you enter it on your laptop.
- Clearing your browser's site data will erase it.
- The "Online Orders" storefront feature (customers placing orders) only works
  if the customer and the admin are using **the same browser** in this local
  setup, since localStorage isn't shared across devices.

To get real multi-device sync (your phone, your staff's phone, and customers
ordering from their own phones all seeing the same data), you'd need to connect
this app to a real backend/database — for example Firebase, Supabase, or a custom
Node.js + PostgreSQL API. That's a solid next step once you've tried this
prototype and know which features you actually want to keep. Happy to help you
plan or build that when you're ready.

## What's real vs. simulated in this prototype

Working for real: GST-calculated invoices/quotations/challans/credit notes,
inventory with low-stock alerts, purchases, party ledgers, BOM-based production,
cash/bank tracking, reports with CSV export, backup/restore as JSON, WhatsApp
share links, UPI QR codes on invoices, print-to-PDF, and a customer storefront.

Not included (needs real infrastructure): multi-device cloud sync, a real
authentication system, barcode scanner hardware support, thermal/Bluetooth
printer drivers, a Windows desktop build, WhatsApp Business API automation, and
payment gateway settlement.
