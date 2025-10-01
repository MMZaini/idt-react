This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## What this app does

IDT Bulk Ordering is a small frontend for automating large oligo/probe orders to IDT.
It uses a modern web stack (Next.js + React, Tailwind, Zod) and a tiny local automation agent that drives a browser (Selenium / Chromedriver)
to eliminate repetitive copy/paste when placing many orders.

Key QoL features (blunt):
- Multi-line editor for oligos and probes (add/remove/insert many rows).
- Per-line validation (DNA IUPAC chars, per-scale length checks) so you catch errors early.
- Import / export JSON, localStorage autosave, and a simple order-code generator.
- Local agent integration: shows agent Online/Offline and can POST prepared lines to a local Selenium agent for automated entry into IDT.

Currently, only ordering oligos is implemented.

Planned next steps:
- Add support for probes.
- Implement extra QoL features such as preset sequences, library of sequences to save to/import from, ect.
- Begin work on BLAST integration and AI-assisted features.
- Expand testing to detect additional IDT errors.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

NOTE: This repository was trimmed to the frontend-only UI and its dependencies. Backend API routes, automation runners, and end-to-end tests were removed to keep a minimal frontend deliverable. If you need the automation/backend restored, let me know and I can re-add them.