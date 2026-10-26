# Serial Scanner — Asset Register PWA

A fast, phone-optimized continuous barcode & QR code scanning Progressive Web App (PWA) built for asset register data collection and instant Excel (`.xlsx`) export.

---

## ✨ Features

- 📷 **Continuous Camera Scanning**: Real-time barcode & QR scanning directly in your mobile browser using `html5-qrcode`.
- ⚡ **Duplicate Detection**: Prevents duplicate entries with warning alerts and optional overrides.
- 🔊 **Haptic & Audio Feedback**: Instant tactile vibrations and audio beeps on successful scans.
- 📝 **Asset Details & Metadata**: Set location, category, model, status, notes, and custom fields per scan or in bulk.
- 📊 **Excel (.xlsx) Export**: One-tap export cleanly formatted for asset import templates using `SheetJS` (`xlsx`).
- 📱 **Progressive Web App (PWA)**: Installable to home screen on iOS and Android with offline service worker support (`sw.js`).
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
