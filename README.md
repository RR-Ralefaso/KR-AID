<centre>
<img src="https://github.com/RR-Ralefaso/KR-AID/blob/code/HA_logo.jpg?raw=true" width="200">
</centre>

# 🏥 KR-AID: Medical Facility Finder & SOS Utility

**KR-AID** (Knowledge & Response Aid) is a specialized Python-based emergency tool designed to bridge the gap between a medical crisis and professional help. By leveraging real-time geolocation and OpenStreetMap data, it identifies the nearest medical facilities and provides instant walking routes for the user.

---

## 🌟 Overview
In an emergency, every second counts. KR-AID simplifies the process of finding help through a four-step automated pipeline:

1.  **Locate:** Automatically detects user coordinates via IP geocoding.
2.  **Scan:** Searches the surrounding area for hospitals and clinics using the Overpass API.
3.  **Visualize:** Renders an interactive map within a high-performance PyQt5 GUI.
4.  **Route:** Generates a direct, turn-by-turn walking path to the chosen facility.

---

## 🛠️ Technical Stack

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **GUI Framework** | `PyQt5` & `QtWebEngine` | Desktop interface and embedded map rendering. |
| **Mapping** | `Folium` | Generates OpenStreetMap-based HTML layers. |
| **Data Retrieval** | `Requests` & `Overpass API` | Real-time spatial queries for medical infrastructure. |
| **Routing Engine** | `OpenRouteService` | Calculates walking paths and travel duration. |
| **Geocoding** | `Geocoder` | IP-based initial location services. |

---

## 🚀 Features

* **SOS Logic:** Optimized for speed; the app identifies your location and nearby aid immediately upon startup.
* **Smart Proximity Search:** Queries for `amenity="hospital"` within a 5000m radius (customizable).
* **Live Route Rendering:** Displays a green walking path from your current position to the facility using GeoJSON.
* **Emergency Metadata:** Automatically extracts names, addresses, and phone numbers from OSM tags.

---

## ⚙️ Setup & Installation

### 1. Prerequisites
* **Python 3.8+**
* **API Key:** Obtain a free API key from **[OpenRouteService](https://openrouteservice.org/)** to enable routing features.

### 2. Install Dependencies
Clone the repository and install the required libraries:

```bash
# Clone the repository
git clone [https://github.com/yourusername/KR-AID.git](https://github.com/yourusername/KR-AID.git)
cd KR-AID

# Install requirements
pip install PyQt5 PyQtWebEngine folium geocoder openrouteservice requests pandas
