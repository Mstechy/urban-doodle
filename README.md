# BeautyGlow — Next.js + Tailwind minimal e-commerce starter

This is a GitHub-ready Next.js (App Router) + Tailwind CSS starter for the BeautyGlow store.
It uses **localStorage** for data (products, cart, orders) so you can run and test without a backend.
Paystack integration is wired client-side (uses `NEXT_PUBLIC_PAYSTACK_KEY`), and a serverless
verification API (`/api/verify-payment`) is included — set `PAYSTACK_SECRET_KEY` in your deployment
environment (Vercel) to enable server-side verification.

## Features
- Home, Shop (filters), Product detail, Cart, Checkout (Paystack), Order status, Admin
- Admin can mark orders as `successful` or `failed` (client-side)
- Countdown timer at checkout (10 minutes)
- Newsletter wired to Formspree (`https://formspree.io/f/mwpnklkk`)
- Tailwind CSS for responsive UI

## Quick start (locally)
```bash
# clone repo or unzip the project
npm install
# add env (see .env.example)
npm run dev
```

## Deploy to Vercel
1. Create a GitHub repo and push this project.
2. On Vercel, import the repo and set environment variables:
   - `NEXT_PUBLIC_PAYSTACK_KEY` = your Paystack public key (pk_test_...)
   - `PAYSTACK_SECRET_KEY` = your Paystack secret key (sk_test_...) (do NOT commit this)
3. Deploy.

