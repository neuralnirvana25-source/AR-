
# IRG Grand AR Menu (Hybrid)

**Android (Chrome):** True AR with camera + plane detection via WebXR (Three.js).  
**iOS (Safari):** Native AR via Quick Look (`.usdz`) using `rel="ar"`.  
**Fallback:** 360° viewer with `<model-viewer>`.

## Run Locally
- Desktop: `python -m http.server 8000` → open `http://localhost:8000`
- Phone testing requires **HTTPS** for camera access (WebXR). Quick options:
  - Host on Netlify/Vercel/GitHub Pages (free HTTPS)
  - Or use a tunnel (e.g., `npx localtunnel --port 8000`) to get an HTTPS URL

## Add Your Dishes
- Put images in `/images/` and models in `/models/`
- Edit `items.json` to point to your files (`.glb` + `.usdz` for each item)
- Ensure **real-world scale** (plate ≈ 0.25m)

## Notes
- If AR button opens the 360° viewer on Android: device/browser might not support WebXR or page not served over HTTPS.
- On iOS, AR opens Quick Look — camera turns on there.
