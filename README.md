#📡 Spatial Optimization of Telecom Network Coverage and Customer Demand in Greater Accra

Final Map Preview
<p align="center">
  <img src="https://github.com/frankraDIUM/Spatial-Optimization-of-Telecom-Network-Coverage-and-Customer-Demand-in-Greater-Accra/blob/main/Interactive%20map.png" />
</p>
--

Dashboard Metrics
<p align="center">
  <img src="https://github.com/frankraDIUM/Spatial-Optimization-of-Telecom-Network-Coverage-and-Customer-Demand-in-Greater-Accra/blob/main/Telecom.png" />
</p>
--

## Project Overview
End-to-end geospatial project to identify coverage gaps and recommend optimal new cell tower locations in Greater Accra, Ghana. 
The solution combines telecom tower data, high-resolution population density, roads, terrain, and land use to generate ranked candidate sites using Multi-Criteria Decision Analysis (MCDA).

**Objective**: Support data-driven network expansion decisions by combining telecom tower data, high-resolution population density, roads, slope, and land use constraints.

## Key Features
- Dynamic coverage modeling using OpenCelliD tower range data
- Underserved population quantification (~565,000 people identified)
- DBSCAN clustering of high-density gap zones
- Full MCDA scoring: Population served, distance to existing towers, road accessibility, slope, and land use constraints (ESA WorldCover 2021)
- Ranked top 20 candidate tower locations
- Interactive Folium map and Power BI dashboard

## Technologies Used
- **Python**: GeoPandas, Rasterio, Scikit-learn, SciPy, Folium, Contextily, Pandas, NumPy
- **GIS**: QGIS (validation & clipping)
- **Visualization**: Power BI, Matplotlib, Folium (HTML)
- **Data**: OpenCelliD, WorldPop 2020, ESA WorldCover 2021, OSM Roads, SRTM DEM

## Results
- **Population coverage rate**: 89.3% (dynamic buffers)
-  **Underserved population**: ~564,832 (10.7% of 5.295 million)
- **Clusters identified**: 8 (after filtering)
- **Top candidates**: Ranked by full MCDA score (see `top_tower_candidates_full_mcda.geojson`)

## Interactive Map
Open: [`top_candidates_interactive_full.html`](top_candidates_interactive_full.html)  
(zoom, click markers for pop served, distances, slope, land use, score)

