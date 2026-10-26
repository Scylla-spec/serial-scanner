# Serial Scanner — Asset Register PWA

A fast, phone-optimized continuous barcode & QR code scanning Progressive Web App (PWA) built for asset register data collection and instant Excel (`.xlsx`) export.

---

## ✨ Features in ENTERPRISE Edition

- 📋 **Full Asset Register Alignment (All 13 Columns Supported)**:
  - 🏷️ **Asset Category (Type - Col C)**: 14 categorized options (`PRINTER / COPIER`, `DESKTOP PC / WORKSTATION`, `LAPTOP`, `MONITOR`, `POS TERMINAL`, `RECEIPT PRINTER`, `BARCODE SCANNER`, `NETWORK SWITCH`, `UPS / POWER`, `SERVER`, `CCTV`, etc.).
  - 📦 **Asset Name & Model (Col A)**: Linked dropdown dynamically displaying matching models for the selected category (e.g. selecting *PRINTER* shows *Epson printer*, *Epson EcoTank*, *HP LaserJet*, *Canon*, etc.; selecting *DESKTOP PC* shows *Dell OptiPlex*, *HP EliteDesk*, *Lenovo ThinkCentre*). Includes `+ Type Custom Model...`.
  - 🏪 **Shop / Store / Department (Col H)**: Dropdown featuring all corporate units and retail brands (`Head Office`, `Chicken Inn`, `Pizza Inn`, `Bakers Inn`, `Creamy Inn`, `Galito's`, `Steers`, `IT Workshop`, `Central Kitchen`, `Finance`, plus `+ Add Custom Shop...`).
  - 🏢 **Site Location / Complex (Col I)**: Comprehensive complex dropdown (`TV City Complex`, `Head Office Complex`, `Joina City`, `Sam Levy's Village`, `Msasa Depot`, `Graniteside`, `Belmont Bulawayo`, `Speke Ave`, `Avondale`, `Gweru`, `Mutare`, plus `+ Add Custom Site...`).
  - ⭐ **Condition (Col J)**: `Good / Operational`, `New / Unopened`, `Excellent`, `Fair / Functional`, `Poor`, `Faulty / For Repair`.
  - 📅 **Purchase / Audit Date (Col G)**: Date picker stamping the audit date for every unit.
- ⚡ **Low-Light & Dim Environment Booster**:
  - **Hardware ML BarcodeDetector**: Direct native acceleration for instant barcode decode even under poor lighting, steep angles, or blurry motion.
  - **⚡ Boost Button**: Real-time high-contrast digital filter (`contrast(1.6) brightness(1.35)`) making faint barcode lines pop against dark surfaces.
  - **🔦 Fixed Torch & Screen Illuminator**: Reliable flashlight activation via `MediaStreamTrack` with an automatic bright screen floodlight fallback.
  - **🔍 1x / 2x Zoom**: Scan tiny barcode stickers without casting a phone shadow.
- 📷 **Continuous High-Res Scanning**: 1080p stream with dynamic wide-aspect reticle tuned for 1D asset serial labels and 2D QR codes.
- ⚡ **Duplicate Detection**: Prevents duplicate entries with warning alerts and optional overrides.
- 🔊 **Haptic & Audio Feedback**: Instant tactile vibrations and audio beeps on successful scans.
- 📊 **Excel (.xlsx) Export**: One-tap export cleanly formatted for asset import templates using `SheetJS` (`xlsx`) matching all columns A–M.
- 📱 **Progressive Web App (PWA)**: Installable to home screen on iOS and Android with v3 offline service worker support (`sw.js`).
- 🛡️ **Zero Backend Dependency**: 100% client-side privacy-first architecture; all asset registers remain in local storage on your device.
- 🌐 **GitHub Pages Ready**: Can be hosted freely on GitHub Pages with zero build steps!

---

## 🚀 Quick Start (Local Development)

Because this is built with standard HTML5, CSS3, and modern JavaScript, no build steps are required.

### Using Python:
```bash
python -m http.server 8000
```
Then navigate to `http://localhost:8000` (or `https://` if testing camera permissions on mobile devices over your local network).

### Using Node.js:
```bash
npx serve .
```

> **Note on Camera Permissions**: Modern mobile browsers (iOS Safari and Android Chrome) require **HTTPS** (or `localhost`) to access camera hardware. If serving across your local Wi-Fi to a physical phone, consider using an HTTPS tunnel such as Cloudflare Tunnel (`cloudflared`) or ngrok.

---

## 🌐 Deploy to GitHub Pages

1. Push this repository to GitHub.
2. In your GitHub repository, go to **Settings** > **Pages**.
3. Under **Build and deployment** > **Source**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder, then click **Save**.
5. Your scanner will be live on `https://<your-username>.github.io/<repo-name>/` with full HTTPS camera support!

---

## 📁 Project Structure

```
serial-scanner/
├── index.html              # Core application UI, styles, and logic
├── manifest.json           # PWA web app manifest
├── sw.js                   # Service worker for offline caching
├── icon.svg                # Vector app icon
├── html5-qrcode.min.js     # Barcode / QR camera scanner library
├── xlsx.full.min.js        # SheetJS Excel exporter
├── .gitignore              # Ignored executables and temp files
└── README.md               # Documentation
```

---

## 📄 License

MIT License. Free for personal and commercial asset tracking use.
