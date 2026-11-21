# GTA Generation – Then & Now

Web app (MVP) to compare two personal photos across two GTA eras:
- **GTA 5 era (2013)** – photo from around 2013
- **GTA 6 era (2026)** – recent photo

The app generates a cinematic "then & now" comparison image locally in the browser.

## Features (MVP)
- Immersive landing page with GTA V / GTA VI logo slots and FR/EN toggle
- Upload two photos (JPG, JPEG, PNG, WEBP) with preview, replace, remove
- Portrait crop/adjustment (3:4) to harmonize both photos
- Automatic composition: logos, 2013/2026 labels, vertical VS divider, bottom tagline
  - EN: `13 YEARS LATER...` / `Same Player. Different Generation.`
  - FR: `13 ANS PLUS TARD...` / `Même joueur. Nouvelle génération.`
- Export in 3 formats:
  - 1080×1080 (Instagram square)
  - 1080×1350 (Instagram portrait)
  - 1080×1920 (TikTok / Stories)
- Download as PNG or JPEG, share via Web Share API when available
- Client-side processing (Canvas). No account, no payment, no permanent storage.

## Tech stack
- React + Vite
- Tailwind CSS
- `react-easy-crop` for cropping
- `lucide-react` icons
- HTML Canvas for rendering/export

## Prerequisites
- Node.js 18+ and npm

## Run locally
```bash
npm install
npm run dev
```
Then open the URL shown by Vite (usually http://localhost:5173).

## Build
```bash
npm run build
npm run preview
```

## Official logos
Logo areas are provided as placeholders/slots in the UI and generated image. If you have rights to use official GTA V / GTA VI logo assets, you can place them in `public/logos/` (e.g. `gta-v.png`, `gta-vi.png`) and extend the app to render them instead of text slots. Do not use assets without authorization.

## Privacy
Images are read and processed in the browser. The MVP does not upload photos to a server or store them permanently.

## Manual test checklist
- [ ] Upload JPG/JPEG/PNG/WEBP for both slots
- [ ] Replace and remove photos
- [ ] Crop/adjust both portraits and regenerate
- [ ] Verify alignment/dimensions of portraits in output
- [ ] Export all 3 formats (1080×1080, 1080×1350, 1080×1920) as PNG and JPEG
- [ ] Test on mobile and desktop layouts
- [ ] Test FR/EN toggle
- [ ] Confirm no network upload of photos (browser devtools) during normal use
