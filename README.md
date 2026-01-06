# Urban Accessibility Analysis: Ethiopia

## 📍 Project Overview
This project analyzes population distribution across Ethiopia at multiple administrative levels — **Woreda**, **Zone**, and **Region** — using geospatial and raster data. It supports urban accessibility planning by identifying demographic concentrations and spatial patterns.

---

## 📂 Data Sources
- **Population Raster**: WorldPop 2020, 100m resolution, resampled to 1km for computational efficiency.
- **Administrative Boundaries**: GADM-derived GeoPackage (`Ethiopia_All`) with Region, Zone, and Woreda layers.
- **Cleaned Woreda Boundaries**: `woredas_cleaned` layer in `ethiopia_accessibility.gpkg`.

---

## 🧭 Methodology

### 1. Raster Preprocessing
- Resampled 100m population raster to 1km using average aggregation.
- Verified resolution and dimensions for consistency with vector layers.

### 2. Zonal Statistics
- Computed total population (`pop_sum`) and average density (`pop_mean_density`) per Woreda using zonal statistics.
- Reprojected all vector layers to **EPSG:4326** to ensure valid spatial joins.

### 3. Spatial Joins & Aggregation
- Joined Woredas with Zones and Regions using `gpd.sjoin(..., predicate="intersects")`.
- Aggregated population statistics at:
  - **Woreda level** → `woredas_population_summary.csv`
  - **Zone level** → `zones_population_summary.csv`
  - **Region level** → `regions_population_summary.csv`

---

## 📊 Visualizations

### 🔹 Bar Chart: Total Population by Region
- Highlights demographic weight of each Region.
- Sorted for easy comparison.

### 🔹 Choropleth Maps
- **Map 1**: Total population by Region (shaded by `pop_sum`)
- **Map 2**: Average population density by Region (shaded by `pop_mean_density`)
- **Zone names labeled** on both maps for geographic clarity.

---

## 📦 Outputs
- `ethiopia_accessibility.gpkg` → cleaned Woreda geometries.
- `eth_pop_1km.tif` → resampled population raster.
- `woredas_population_summary.csv` → Woreda-level stats.
- `zones_population_summary.csv` → Zone-level stats.
- `regions_population_summary.csv` → Region-level stats.
- Side-by-side maps and bar charts embedded in notebook.

---

## 🧠 Key Insights
- Oromia and Amhara dominate in total population.
- Addis Ababa and Dire Dawa show high density despite small area.
- Choropleth maps reveal spatial disparities critical for accessibility planning.

---

## 🛠️ Tools Used
- Python, GeoPandas, Rasterio, Matplotlib
- Jupyter Notebook (Kaggle environment)

---

## 👤 Author
**Aron**  
Chief Information & Technology Officer | Data Scientist | GIS Enthusiast  
[LinkedIn](#) | [GitHub](#) | [Kaggle](#)