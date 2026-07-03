# 📦 iContainers Shipment Dashboard

A modern, professional HTML5 dashboard for tracking ocean freight shipments from iContainers with real-time status updates and documentation management.

## 🎯 Features

- **📊 Summary Dashboard**: Overview of shipments at a glance
  - Total shipments count
  - Confirmed vs. in-transit breakdown
  - Estimated Time of Arrival (ETA)

- **📦 Shipment Cards**: Detailed view for each booking
  - Booking ID and status badges
  - Departure and ETA dates
  - Bill of Lading (B/L) number
  - Shipment type and details

- **📄 Documentation Tracking**
  - Real-time status indicators
  - Green checkmarks for completed documents
  - Orange warnings for pending items
  - Quick reference for required submissions

- **📅 Update Timeline**
  - Recent shipment history
  - Event timestamps
  - Status change notifications

- **🎨 Modern Design**
  - Dark theme with gradient accents
  - Fully responsive (mobile, tablet, desktop)
  - Glassmorphism UI components
  - Smooth animations and transitions

- **⚙️ Utilities**
  - 🖨️ Print to PDF functionality
  - 💾 Export data as JSON
  - 🔄 Real-time refresh capability
  - Auto-timestamp updates

## 📋 Files

```
icontainers-dashboard/
├── index.html          # Main dashboard (all-in-one file)
├── shipments.json      # Shipment data (load dynamically)
└── README.md          # This file
```

## 🚀 Quick Start

### Option 1: Local File
Simply open `index.html` in your web browser:
```bash
open index.html
# or
firefox index.html
```

### Option 2: Local Server
Serve locally with Python:
```bash
python3 -m http.server 8888
# Then visit: http://localhost:8888
```

### Option 3: Deploy to GitHub Pages
1. Fork or clone this repository
2. Push to GitHub
3. Enable GitHub Pages in repository settings
4. Dashboard will be available at: `https://yourusername.github.io/icontainers-dashboard`

## 📊 Data Structure

The `shipments.json` file contains:
```json
{
  "shipments": [
    {
      "id": "booking_id",
      "type": "Ocean LCL",
      "status": "confirmed|in_transit",
      "departure_date": "ISO date",
      "eta_date": "ISO date",
      "documentation": {
        "document_name": {
          "status": "completed|pending|active",
          "label": "Display name"
        }
      },
      "updates": [
        {
          "date": "ISO date",
          "message": "Update message",
          "by": "Source"
        }
      ],
      "notes": ["Warning or note"]
    }
  ],
  "summary": {
    "total_shipments": 3,
    "confirmed": 2,
    "in_transit": 1,
    "eta": "2026-07-30",
    "pending_docs": "List of pending documentation"
  }
}
```

## 🎨 Customization

### Update Shipment Data
Edit `shipments.json` with your actual shipment information. The dashboard will automatically reload the data.

### Change Colors
Modify CSS variables in the `<style>` section of `index.html`:
- Primary gradient: `#60a5fa` → `#34d399` (blue to green)
- Status colors: Edit `.status-confirmed`, `.status-in-transit`
- Accent colors: Edit background and text colors

### Add More Shipments
Simply add new objects to the `shipments` array in `shipments.json`.

## 📱 Responsive Design

The dashboard is optimized for:
- 📱 Mobile phones (320px+)
- 📱 Tablets (768px+)
- 💻 Desktops (1024px+)
- 🖥️ Ultra-wide screens (1440px+)

## 🖨️ Print & Export

- **Print to PDF**: Click "Print / PDF" button → Select "Save as PDF"
- **Export Data**: Click "Export Data" to download shipment data as JSON
- **Refresh**: Click "Refresh" to reload data from `shipments.json`

## 🔐 Privacy & Data

- **No external APIs**: All data stays local
- **No tracking**: No analytics or third-party services
- **Client-side only**: Dashboard runs entirely in your browser
- **Anononymized data**: Real client/employee names replaced with generic labels

## 📝 Browser Support

- Chrome/Chromium 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 🔄 Updates & Maintenance

To update shipment data:
1. Edit `shipments.json`
2. Click "Refresh" in the dashboard
3. Changes appear instantly

## 📧 Support

For issues or questions, please refer to the shipment data structure and ensure JSON formatting is valid.

---

**Version**: 1.0  
**Created**: July 3, 2026  
**Last Updated**: July 3, 2026  
**Status**: ✅ Production Ready

**Dashboard Tools Used**:
- HTML5 & CSS3 (Flexbox/Grid)
- Vanilla JavaScript (No frameworks)
- JSON data format
- Web Storage API

---

*Built with 💙 for efficient shipment tracking*
