# leaflet-challenge

# Earthquake Visualization

This project visualizes earthquake data using a dynamic, interactive map created with the Leaflet.js library. It pulls data from the USGS GeoJSON Feed, providing real-time earthquake information, including location, depth, and magnitude. The visualization fulfills the requirements outlined below.

## Requirements and Features

### **Dataset**

- **Source**: USGS GeoJSON Feed ([Earthquake Data API](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php)).
- **Selection**: Data set includes all earthquakes from the past week (`all_week.geojson`).

### **Visualization Tasks**

1. **Data Loading**:

   - Earthquake data is fetched using D3.js from the USGS GeoJSON Feed URL
   - Data points are parsed to extract longitude, latitude, depth, and magnitude
2. **Map Initialization**:

   - A Leaflet.js map is centered on the continental United States (`39.8283, -98.5795`) with zoom level `4`
   - The OpenStreetMap TileLayer loads without errors
3. **Markers**:

   - **Size**: Circle markers' sizes reflect earthquake magnitudes (`radius = magnitude * 5`)
   - **Color**: Markers are color-coded based on depth:
     - Green for shallow depths
     - Yellow to orange for moderate depths
     - Dark red for deep earthquakes
   - **Position**: Markers are plotted based on earthquake coordinates (longitude, latitude)
4. **Popups**:

   - Each marker includes a popup displaying:
     - Magnitude
     - Depth (in kilometers)
     - Location description (e.g., city or region)
5. **Legend**:

   - A legend is included on the map to explain depth ranges and their corresponding colours
   - Depth ranges: `0–30 km`, `30–50 km`, `50–70 km`, `70–90 km`, `90+ km`

## Implementation Details

### **Technologies Used**

- **JavaScript**: Primary language for logic and rendering.
- **Leaflet.js**: For map rendering and interactivity.
- **D3.js**: For data fetching and processing GeoJSON earthquake data.
- **OpenStreetMap**: Provides map tiles for visualization.
