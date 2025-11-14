# Deft Barcode Scanner

A powerful **Progressive Web App (PWA)** for real-time barcode and QR code scanning with advanced webhook integration. Built with modern web technologies and optimized for mobile devices.

![PWA Ready](https://img.shields.io/badge/PWA-Ready-blue)
![Browser Support](https://img.shields.io/badge/Browser-Chrome%20%7C%20Firefox%20%7C%20Safari%20%7C%20Edge-green)

---

## Overview

**Deft Barcode Scanner** is a responsive web application for real-time barcode and QR code scanning directly in the browser. Powered by the **html5-qrcode** library, it delivers fast dense-QR detection, smooth performance, and reliable scanning across devices with camera support.

---

## Features

- 📱 **Real-time Scanning** – Instant detection with optimized performance  
- 🔗 **Webhook Integration** – Auto-send scanned data to your endpoint  
- 📚 **Webhook History** – Save & reuse up to 10 URLs  
- 🎯 **Multi-Format Support** – 1D + 2D barcode formats  
- 📲 **PWA Support** – Install as a mobile app  
- 💾 **Local Storage** – Persistent settings  
- 📱 **Mobile Optimized** – Fully responsive  
- 🔊 **Audio Feedback** – Beep on successful scans  
- 🌐 **Online/Offline Status** – Live connectivity monitoring  
- ⚙️ **Camera Optimization** – Prefers back/environment camera  

---

## Supported Formats

### 2D Codes
- QR Code  
- Data Matrix  
- Aztec  
- PDF417  

### 1D Linear Barcodes
- UPC-A/E  
- EAN-8/13  
- Code 128  
- Code 39  

---

## Quick Start

### Configure Settings (Optional)
1. Open **Settings**  
2. Enter your **Webhook URL**  
3. Click **💾 Save Settings**

### Start Scanning
1. Tap **📷 Start Scanner**  
2. Point the camera at the barcode/QR code  
3. View results under **Current Scan**

### Webhook History
- Click the webhook input to view past URLs  
- Select from up to **10 saved entries**

---

## Optimal Scanning Tips

**For Dense QR Codes**
- Distance: 6–10 inches  
- Lighting: Bright, even lighting  
- Steady: Hold still 2–3 seconds  
- Angle: Keep device flat and parallel  
- Fill Frame: QR code should fill most of the camera view  

**General**
- Well-lit environment  
- 4–12 inches from code  
- Avoid extreme angles  
- Keep device steady  

---

## Camera Requirements

**Minimum**
- 720p resolution  
- Auto-focus  
- Modern browser  

**Recommended**
- 1080p or higher  
- Continuous auto-focus  
- Optical image stabilization  

---

## Webhook Configuration

### Data Format
```json
{
  "barcode_data": "scanned_data_here",
  "timestamp": "2025-01-01T12:00:00.000Z",
  "scanned_at": "2025-01-01T12:00:00.000Z",
  "code_type": "QR_CODE"
}

HTTP Request
Method: POST
Content-Type: application/json
Endpoint: Your configured webhook URL

Webhook History
Auto-saves up to 10 recent URLs
Accessible by clicking the input field

Performance
Metric	Value
Scan Speed	1–3 seconds
Success Rate	90%+ (ideal conditions)
Camera Startup	1–2 seconds
History Limit	10 URLs
Supported Formats	10+ barcode types

Technical Details
Browser Support
Chrome 60+
Safari 11+
Firefox 55+
Edge 79+

Dependencies
html5-qrcode
Native Web APIs (camera, localStorage, AudioContext)
PWA (service worker, manifest)

Storage
Webhook URLs: localStorage
Webhook History: localStorage (10 entries)
Scan Data: session only
Settings: persistent

Troubleshooting
Camera Access Denied
Check browser permissions
Refresh the page

Scanner Won’t Start
Ensure no other app is using camera
Try another browser

Delay Before Camera Opens
App includes 1-second initial scan protection (normal behavior)

No Sound
Check volume / silent mode
Some browsers require user interaction first

Webhook Not Sending
Check internet connection
Validate URL & CORS
Ensure endpoint accepts POST JSON

Technical Architecture
Library Info
Powered by html5-qrcode
Optional BarcodeDetector API support
30 FPS scanning, optimized for QR codes

Project Structure
pgsql
Copy code
deft-barcode-scanner/
├── index.html
├── manifest.json
└── service-worker.js

Key Features
1-second scan protection
Automatic back-camera selection
Robust permission/error handling
Optimized for dense QR codes

License
© 2025 Deftmind Technology and Media Ventures

Support
For support, feature requests, or bug reports, contact Deftmind Technology and Media Ventures.