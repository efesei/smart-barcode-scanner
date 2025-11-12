# Deft Barcode Scanner

![Version](https://img.shields.io/badge/Version-1.1-blue.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-green.svg)
![Browser Support](https://img.shields.io/badge/Browser-Chrome%20%7C%20Safari%20%7C%20Firefox%20%7C%20Edge-orange.svg)

A powerful web-based barcode and QR code scanning application that supports real-time detection with webhook integration.

## Overview

Deft Barcode Scanner is a responsive web application that enables real-time barcode and QR code scanning directly from your browser. Built with modern web technologies, it provides a seamless scanning experience across all devices with camera capabilities.

## Features

- 📱 **Real-time Scanning** - Instant detection without manual capture
- 🔗 **Webhook Integration** - Automatic data transmission to endpoints
- 📚 **Webhook History** - Save and reuse previous webhook URLs
- 🔄 **Auto-Recovery** - Self-healing scanner with manual refresh
- 📲 **PWA Support** - Install as native app on mobile devices
- 🎯 **Multi-Format Support** - Comprehensive barcode and QR code compatibility
- 💾 **Local Storage** - Settings persist across sessions
- 📱 **Mobile Optimized** - Responsive design for all screen sizes

## Supported Formats

### 2D Codes
- QR Codes
- Data Matrix
- PDF417

### 1D Linear Barcodes
- UPC-A/E
- EAN-8/13
- Code 128
- Code 39

## Quick Start

### Basic Usage

1. **Configure Settings (Optional)**
   - Open the Settings section
   - Enter your webhook URL (optional)
   - Click "Save Settings"

2. **Start Scanning**
   - Click "Start Scanner" to activate camera
   - Point camera at barcode/QR code
   - Scanner automatically detects and captures data
   - View results in the Current Scan section

3. **Webhook History**
   - Click the webhook URL field to see recent entries
   - Select from previously used URLs
   - History automatically saves on settings save

### Optimal Scanning Conditions

- **Lighting:** Well-lit environment, avoid direct glare
- **Distance:** 4-12 inches from code
- **Angle:** Direct facing, avoid extreme angles
- **Stability:** Keep device steady during scanning

## Camera Requirements

### Minimum Specifications
- **Resolution:** 720p (1280×720)
- **Focus:** Auto-focus capability
- **Browser:** Modern browser with camera support

### Recommended Specifications
- **Resolution:** 1080p (1920×1080) or higher
- **Focus:** Continuous auto-focus
- **Features:** Optical image stabilization, good low-light performance

## Webhook Configuration

### Data Format

```json
{
  "barcode_data": "scanned_data_here",
  "timestamp": "2025-01-01T12:00:00.000Z",
  "scanned_at": "2025-01-01T12:00:00.000Z",
  "code_type": "QR_CODE"
}
```

### HTTP Request
- **Method:** POST
- **Content-Type:** application/json
- **Endpoint:** Your configured webhook URL

### Webhook History
- Automatically saves up to 10 recent webhooks
- Access by clicking the webhook URL input field
- Maintains full backward compatibility

## Performance

| Metric | Value |
|--------|-------|
| Scan Speed | 1-3 seconds (typical) |
| Success Rate | 90%+ (optimal conditions) |
| Reset Time | 1.5 seconds |
| History Limit | 10 webhooks |

## Troubleshooting

### Common Issues

**Scanner won't start**
- Check camera permissions in browser settings
- Ensure no other app is using the camera

**Poor detection quality**
- Improve lighting conditions
- Clean camera lens
- Hold device steady
- Move closer to smaller codes

**Animation stuck**
- Use the "Fix Scanner" button
- Refresh the page if necessary

**No sound on scan**
- Check device volume settings
- Ensure device is not in silent mode

**Webhook not sending**
- Verify internet connectivity
- Check webhook URL format
- Ensure CORS policies allow requests

### For Dense Barcodes
- Use higher resolution cameras
- Ensure excellent lighting conditions
- Get closer to the barcode
- Use continuous focus mode

## Technical Details

### Browser Support
- Chrome 60+
- Safari 11+
- Firefox 55+
- Edge 79+

### Storage
- **Webhook URLs:** localStorage (persists until cache cleared)
- **Scan Data:** Current session only
- **Settings:** Persistent across browser sessions

### Dependencies
- **ZXing Library** - Barcode decoding
- **Native Web APIs** - Camera access, localStorage

## Development

### Project Structure

```
deft-barcode-scanner/
├── index.html          # Main application file
├── manifest.json       # PWA manifest
└── service-worker.js   # Service worker (if implemented)
```

### Local Development

1. Serve the HTML file using any web server
2. Access via HTTPS for camera permissions
3. Test with various barcode types

## License

Copyright © 2025 Deftmind Technology and Media Ventures

## Support

For technical support, feature requests, or bug reports, please contact Deftmind Technology and Media Ventures.

---

**Note:** This application works best in well-lit conditions with clear, undamaged barcodes. Performance may vary based on camera quality and environmental factors.
