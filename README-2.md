# PK Hosting Mobile App (Prototype)

A mobile-first app prototype for [PKHosting.com](https://www.pkhosting.com), designed to match the existing website's brand, content, and customer journey.

**Live demo:** `<add your live URL here>`

## Overview

PK Hosting is a Pakistan-based hosting provider (hosting, domains, VPS, dedicated servers) with local support. This prototype turns the main customer journey into a clean, touch-friendly app: browse plans, find a domain, use free tools, and reach support. Ordering and billing continue on pkhosting.com.

## Brand Alignment

- Primary green `#138a3d` (the site's theme color), light theme with automatic dark mode
- PKR pricing and the same plan names, copy, and tone as the website
- Same navigation structure: Hosting, Domains, Tools, Support

## Features

| Screen | What it does |
|---|---|
| **Home** | Hero message, domain search, plan finder, shortlist, key benefits, system status links, accepted payment methods |
| **Plans** | Personal, Business, and Professional plans with Monthly/Annual toggle, side-by-side comparison, shortlist, and direct Order links. Shortcuts to VPS, Dedicated, and Reseller |
| **Domains** | Name search with .com, .pk, .com.pk, .org.pk, and .net.pk options and prices; links to transfer and the .pk guide |
| **Tools** | WHOIS, DNS, SSL, Email checker, Speed test, Domain appraisal; Knowledgebase, FAQ, Blog; services (SSL, migration, web development, WordPress, partner perks) |
| **Support** | One-tap call and email, ticket link, FAQ (support hours, SSL, backups, migration, payments), refund and backup policies |

Also included: light/dark toggle and a shortlist saved on the device.

## Design Decisions

- **Plan finder:** recommends a plan by number of websites (1, 2-5, 6-10, 10+) and points larger needs to VPS or Reseller.
- **No invented data:** plan details, prices, contact info, and policies come from the public site. Domain availability is confirmed on pkhosting.com rather than faked in the app.
- **Handoff to the website:** checkout, ordering, and tickets open on pkhosting.com, so billing logic stays in one place.

## Tech

- Single-file HTML, CSS, and vanilla JavaScript (no build step, no dependencies)
- Responsive, with safe-area support for phones with notches
- `localStorage` for the shortlist (wrapped in try/catch)

## Run Locally

```bash
git clone https://github.com/<your-username>/pkhosting-mobile-app.git
cd pkhosting-mobile-app
open index.html        # or double-click the file
```

For phone-sized preview, open it in a browser and use device emulation, or serve it with `npx serve .`.

## Deploy

- **GitHub Pages:** Settings, then Pages, then select the `main` branch and root folder.
- **Netlify / Vercel:** import the repo or drag and drop the folder.

## Known Limitations

- Prototype only: no login, invoices, or live account data (these need access to the PK Hosting client-area or billing API).
- Domain availability and final prices are confirmed on pkhosting.com.
- Plan data is embedded in the app; it does not update automatically when the website changes.

## Roadmap

1. React Native (Expo) version for iOS and Android
2. Login with My Services and Invoices
3. Push notifications for renewals and downtime
4. In-app domain availability check and ordering
5. Live plan and pricing sync from the PK Hosting backend

## Credits

Built for PK Hosting, a product of TechAbout (Private) Limited.
