# San Francisco Child Care Dashboard

An interactive dashboard for visualizing licensed child care facilities in San Francisco.

## 🎯 Features

- **Interactive Map** with 1,144 child care facilities
- **100% Location Coverage** - All facilities mapped (geocoded or ZIP-based approximation)
- **Advanced Filtering** - Filter by type, status, capacity, ELFA contract, and SFUSD sites
- **Visual Indicators** - Color-coded markers showing facility status and location accuracy
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
