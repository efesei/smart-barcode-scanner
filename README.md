# 🧭 Deft Barcode Scanner

A powerful **web-based barcode and QR code scanning application** that supports real-time detection with webhook integration.

![Version](https://img.shields.io/badge/Version-1.1-blue.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-green.svg)
![Browser Support](https://img.shields.io/badge/Browser-Chrome%20%7C%20Safari%20%7C%20Firefox%20%7C%20Edge-orange.svg)

---

## 📖 Overview
**Deft Barcode Scanner** is a responsive web application that enables real-time barcode and QR code scanning directly from your browser.  
Built with modern web technologies, it provides a seamless scanning experience across all devices with camera capabilities.

---

## 🚀 Features

- 📱 **Real-time Scanning** — Instant detection without manual capture  
- 🔗 **Webhook Integration** — Automatic data transmission to endpoints  
- 📚 **Webhook History** — Save and reuse previous webhook URLs  
- 🔄 **Auto-Recovery** — Self-healing scanner with manual refresh  
- 📲 **PWA Support** — Install as native app on mobile devices  
- 🎯 **Multi-Format Support** — Comprehensive barcode and QR code compatibility  
- 💾 **Local Storage** — Settings persist across sessions  
- 📱 **Mobile Optimized** — Responsive design for all screen sizes  

---

## 🧩 Supported Formats

### 2D Codes
- QR Codes  
- Data Matrix  
- PDF417  

### 1D Linear Barcodes
- UPC-A / UPC-E  
- EAN-8 / EAN-13  
- Code 128  
- Code 39  

---

## ⚡ Quick Start

### Basic Usage
1. **Configure Settings (Optional)**  
   - Open the **Settings** section  
   - Enter your **webhook URL** (optional)  
   - Click **Save Settings**

2. **Start Scanning**  
   - Click **Start Scanner** to activate camera  
   - Point camera at barcode or QR code  
   - Scanner automatically detects and captures data  
   - View results in the **Current Scan** section

3. **Webhook History**  
   - Click the webhook URL field to see recent entries  
   - Select from previously used URLs  
   - History automatically saves on settings save  

---

## 💡 Optimal Scanning Conditions
| Condition | Recommendation |
|------------|----------------|
| **Lighting** | Well-lit environment, avoid direct glare |
| **Distance** | 4–12 inches from code |
| **Angle** | Direct facing, avoid extreme angles |
| **Stability** | Keep device steady during scanning |

---

## 🎥 Camera Requirements

### Minimum Specifications
- **Resolution:** 720p (1280×720)  
- **Focus:** Auto-focus capability  
- **Browser:** Modern browser with camera support  

### Recommended Specifications
- **Resolution:** 1080p (1920×1080) or higher  
- **Focus:** Continuous auto-focus  
- **Features:** Optical image stabilization, good low-light performance  

---

## 🌐 Webhook Configuration

### Data Format
```json
{
  "barcode_data": "scanned_data_here",
  "timestamp": "2025-01-01T12:00:00.000Z",
  "scanned_at": "2025-01-01T12:00:00.000Z",
  "code_type": "QR_CODE"
}
