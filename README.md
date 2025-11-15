# Deft Barcode Scanner

Advanced barcode and QR code scanner with batch scanning mode, offline support, and PWA capabilities.

## 📁 Project Structure

```
barcode-scanner/
├── index.html           ← Main application file
├── manifest.json        ← PWA configuration
├── service-worker.js    ← Offline support & caching
├── icon-96.png          ← App icon (96x96)
├── icon-192.png         ← App icon (192x192)
├── icon-512.png         ← App icon (512x512) 
└── README.md            ← This file
```

## 🚀 Quick Start

### 1. **Create Project Folder**
```bash
mkdir barcode-scanner
cd barcode-scanner
```

### 2. **Add Files**
Copy the following files from the artifacts:
- `index.html`
- `manifest.json`
- `service-worker.js`

### 3. **Create App Icons**

You need to create PNG icons in these sizes:
- **icon-192.png** (192x192) - REQUIRED
- **icon-512.png** (512x512) - REQUIRED
- Optional: 72, 96, 128, 144, 152, 384

**Quick Icon Creation Options:**

**Option A: Use an Icon Generator (Recommended)**
1. Go to https://realfavicongenerator.net/ or https://www.pwabuilder.com/imageGenerator
2. Upload a logo/image (minimum 512x512)
3. Download all generated icons
4. Place them in your project folder

**Option B: Use a Simple Placeholder**
Create a simple colored square as a temporary icon:
- Any image editor (Paint, Photoshop, GIMP)
- Create 512x512 blue square with white barcode icon
- Export as PNG
- Resize to create other sizes

**Option C: Use Online Tools**
- Canva: https://www.canva.com/ (free templates)
- Figma: https://www.figma.com/ (design tool)
- Photopea: https://www.photopea.com/ (online Photoshop)

### 4. **Test Locally**

**Option A: Using Python**
```bash
# Python 3
python -m http.server 8000

# Then open: http://localhost:8000
```

**Option B: Using Node.js**
```bash
# Install http-server globally
npm install -g http-server

# Run server
http-server -p 8000

# Then open: http://localhost:8000
```

**Option C: Using VS Code Extension**
1. Install "Live Server" extension
2. Right-click `index.html`
3. Select "Open with Live Server"

### 5. **Deploy to GitHub Pages**

```bash
# Initialize git
git init
git add .
git commit -m "Initial commit"

# Create repo on GitHub, then:
git remote add origin https://github.com/yourusername/barcode-scanner.git
git branch -M main
git push -u origin main

# Enable GitHub Pages:
# Settings → Pages → Source: main branch → Save
```

Your app will be live at: `https://yourusername.github.io/barcode-scanner/`

## ✨ Features

### Single Scan Mode
- Scan one barcode/QR code at a time
- Camera stops after each scan
- Immediate webhook delivery

### Batch Scan Mode
- Continuous scanning
- Accumulate multiple items
- Duplicate detection (5-second cooldown)
- Send individually or as batch
- Persistent storage (survives refresh)

### PWA Features
- Install as app on mobile/desktop
- Works offline
- Fast loading (cached)
- Fullscreen experience

## 🔧 Configuration

### Webhook Setup
1. Enter your webhook URL in Settings
2. Choose send method (Individual or Batch)
3. Click "Save Settings"

### Webhook Payload Format

**Single Scan:**
```json
{
  "barcode_data": "123456789",
  "timestamp": "2025-01-15T10:30:00.000Z",
  "scanned_at": "2025-01-15T10:30:00.000Z",
  "code_type": "QR_CODE"
}
```

**Batch (when "Send All as Single Batch"):**
```json
{
  "batch": [
    {
      "barcode_data": "123456789",
      "timestamp": "2025-01-15T10:30:00.000Z",
      "code_type": "QR_CODE",
      "sent": false
    }
  ],
  "batch_size": 1,
  "completed_at": "2025-01-15T10:31:00.000Z"
}
```

## 📱 Supported Barcode Formats

- QR Code
- Data Matrix
- Aztec
- PDF 417
- EAN-13
- EAN-8
- Code 128
- Code 39
- UPC-A
- UPC-E

## 🔒 Requirements

- **HTTPS** (required for camera access)
- Modern browser (Chrome, Firefox, Safari, Edge)
- Camera permission

## 🐛 Troubleshooting

### Camera Not Working
1. Check browser address bar for camera permission
2. Ensure URL starts with `https://`
3. Try different browser
4. Restart browser completely

### App Won't Install
1. Must be served over HTTPS
2. Ensure `manifest.json` and icons exist
3. Check browser console for errors

### Offline Not Working
1. Check `service-worker.js` is registered (console logs)
2. Clear browser cache and reload
3. Check Application → Service Workers in DevTools

## 📄 License

Copyright © 2025 Deftmind Technology and Media Ventures

## 🤝 Support

For issues or questions, please open an issue on GitHub.

---

**Built with:**
- [html5-qrcode](https://github.com/mebjas/html5-qrcode) - QR code scanning library
- Progressive Web App technologies
- Vanilla JavaScript (no frameworks)
