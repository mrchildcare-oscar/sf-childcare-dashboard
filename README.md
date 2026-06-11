# San Francisco Child Care Dashboard

An interactive dashboard for visualizing licensed child care facilities in San Francisco.

## 🎯 Features

- **Interactive Map** with 1,144 child care facilities
- **100% Location Coverage** - All facilities mapped (geocoded or ZIP-based approximation)
- **Advanced Filtering** - Filter by type, status, capacity, ELFA contract, and SFUSD sites
- **Visual Indicators** - Color-coded markers showing facility status and location accuracy
- **Shareable Links** - One click copies a link to your exact view (filters + selections + numbers)
- **Responsive Design** - Works on desktop, tablet, and mobile devices

## 📊 Data Coverage

- **Total Facilities**: 1,144
- **Geocoded (Precise)**: 488 facilities
- **ZIP-based (Approximate)**: 656 facilities
- **Coverage**: 100%

### Facility Types:
- Day Care Centers: 370
- Large Family Child Care Homes: 369
- Small Family Child Care Homes: 208
- Infant Centers: 89
- Single Licensed Child Care Centers: 65
- School Age Day Care Centers: 43

## 🗺️ Map Features

- **Status Colors**:
  - 🟢 Green = Licensed
  - 🔴 Red = Closed
  - 🟠 Orange = Inactive
  - 🔵 Blue = Other

- **Location Accuracy**:
  - ⚪ White border = Geocoded (accurate address)
  - 🟠 Orange border = ZIP-based (approximate location)

- **Navigation**:
  - Map restricted to SF boundaries
  - Click markers for facility details
  - Use scroll to zoom, drag to pan
  - Reset button to return to default view

## 🔗 Sharing a View

The dashboard can produce a link to the **exact view you're looking at** — same filters, same selections, same numbers — so you can show someone how a figure was reached.

**To share:**
1. Set up the view you want (tick checkboxes, pick a district/ZIP, toggle the pressure lens, etc.).
2. Click **🔗 Share view** in the top-right of the header. It changes to **✓ Link copied** — the link is now on your clipboard.
3. Paste it into an email, message, or new browser tab.

Whoever opens the link lands on the identical view. (The link in your browser's address bar also updates live as you change filters, so you can copy it from there too.)

**What's captured in the link:**
- **Programs & Sites:** search text, facility type, status, ELFA contract, capacity range, supervisor districts, and the special toggles (SFUSD, Pre-K, TK, Head Start, CSPP, CCTR), plus heatmap/marker visibility
- **Supply & Demand:** the active tab, geographic view (citywide / district / corridor / ZIP), selected district or ZIP, corridor, and the Demand Pressure Lens (on/off + total vs. ELFA mode)

Only settings you've changed appear in the link, so a fresh, unfiltered view produces a clean URL.

**Examples:**
- Programs tab, Head Start facilities only:
  `…/landscape.html?tab=programs&hs=1`
- District 6 with the ELFA Demand Pressure Lens on:
  `…/landscape.html?geo=district&d=6&sat=1&satmode=elfa`

> Copy-to-clipboard requires a secure (HTTPS) page. On the live GitHub Pages site this works automatically; if a browser ever blocks it, a popup shows the link to copy by hand.

## 🚀 Quick Start

### View Online
Visit: [Your GitHub Pages URL will be here]

### Run Locally
1. Clone this repository
2. Start a local web server:
   ```bash
   python3 -m http.server 8000
   ```
3. Open http://localhost:8000 in your browser

## 📁 Files

- `index.html` - Main dashboard (standalone, no dependencies)
- `childcare_all_coordinates.json` - Facility data with coordinates

## 📋 Data Sources

- [ELFA - SF Dept Early Childhood](https://sfdec.org/early-learning-for-all/early-learning-programs/)
- [CCLD - CA Licensing](https://www.ccld.dss.ca.gov/carefacilitysearch/DownloadData)
- [SFUSD Directory](https://www.sfusd.edu/schools/directory)

## 🏷️ License Information

Each facility includes:
- License number
- Facility type
- Address (or ZIP code if unavailable)
- Capacity
- License status
- ELFA contract status
- SFUSD site affiliation (if applicable)

## ⚠️ Data Limitations

- Small Family Child Care Homes (208) have approximate ZIP-based locations
- Large Family Child Care Homes (369) have approximate ZIP-based locations
- Address data may be unavailable for family child care homes due to privacy

## 🛠️ Built With

- HTML5 / CSS3 / JavaScript
- React 18
- Leaflet.js (mapping)
- Leaflet.heat (heatmap)
- Chart.js (statistics)
- OpenStreetMap tiles

## 📝 Notes

This dashboard provides visualization of licensed child care centers and large Family Child Care (FCC) facilities. Location accuracy varies - geocoded facilities show precise addresses while others show approximate locations based on ZIP code centroids with random jittering to prevent marker overlap.

---

🤖 Generated with Claude Code
