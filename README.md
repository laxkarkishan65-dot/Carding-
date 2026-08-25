# CARD — The Vault

A Vite + React + Three.js + GSAP + Lenis re-engineering of the supplied CARD website.

## Source-of-truth data preserved

The implementation uses the latest `index_final.html` source found in the user's library as the business-data reference. It preserves the six package tiers, prices/balances, UPI ID, payment intent, confirmation form, WhatsApp confirmation destination, operator information, Telegram, WhatsApp Channel, Instagram link, and Garena/Free Fire disclaimer.

The original reference is retained at `public/source-reference.html` and the supplied UPI QR is retained at `public/upi-qr.jpg`.

## Stack

- React 19
- Vite
- Three.js
- GSAP + ScrollTrigger
- Lenis
- CSS / GLSL shader material

## Run

```bash
npm install
npm run dev
```

## Production

```bash
npm run build
npm run preview
```

The runtime is adaptive: lower DPR and particle count on smaller screens, CSS/HTML presentation remains available if WebGL cannot initialize, and `prefers-reduced-motion` removes cinematic motion.

## Payment notes

The site only prepares a UPI intent and WhatsApp confirmation message. It does **not** claim automatic payment verification. The user must attach the selected screenshot in WhatsApp; the operator verifies the UTR/screenshot before delivery.
