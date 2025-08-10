# Sustainable Design Lab - Prototype (Client-side Model Builder)

This React + Vite project now includes a fully client-side **Interactive Model Builder** on the Demo page.

## Features (client-side)
- Parametric module grid editor (columns, rows, module size)
- Storeys and orientation controls
- Built-in materials library with simple thermal (U-value) and embodied carbon (kgCO₂e/m²) entries
- Instant proxy calculations for embodied carbon and a simplified operational energy estimate
- Save/load models in browser (localStorage), export JSON and PNG
- No external simulation services required — everything runs in the browser

## How to run locally
1. Install Node.js (v18+) and npm.
2. In the project directory run:
   ```bash
   npm install
   npm run start
   ```
3. Open http://localhost:5173 in your browser.
4. Go to **Demo** to use the client-side model builder.

## Accuracy notes
- The operational energy and solar index are **approximate proxies** intended for quick comparison and iteration. They are not a replacement for full dynamic simulation (EnergyPlus/Honeybee) for regulatory or certification purposes.
- Embodied carbon values in the built-in library are illustrative. Replace with manufacturer EPD values for procurement-level decisions.

## Deploy to Vercel (one-click using Vercel CLI)
1. Install Vercel CLI: `npm i -g vercel`
2. Log in: `vercel login`
3. From project root run: `vercel --prod` and follow prompts (accept recommended settings).
4. Alternatively, push the repo to GitHub and import into Vercel via the Vercel dashboard for continuous deploys.

## Notes about further extensions
- If you'd like server-side exports (PDF generation with more detailed reports, or heavy simulations), I can scaffold a FastAPI backend and show how to connect it.
- I can also prepare a GitHub repo and provide exact git commands if you want me to push the code there for you.
