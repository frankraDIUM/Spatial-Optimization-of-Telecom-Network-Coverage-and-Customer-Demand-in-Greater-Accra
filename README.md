# Spatial Optimization of Telecom Network Coverage and Customer Demand in Greater Accra

Final Map Preview
<p align="center">
  <img src="https://github.com/frankraDIUM/Spatial-Optimization-of-Telecom-Network-Coverage-and-Customer-Demand-in-Greater-Accra/blob/main/Interactive%20map.png" />
</p>

## Project Overview
This project develops a geospatial framework to identify coverage gaps, quantify the underserved population, and recommend optimal new cell tower locations in Greater Accra, Ghana.

**Objective**: Support data-driven network expansion decisions by combining telecom tower data, high-resolution population density, roads, slope, and land use constraints.

**Key Deliverables**:
- Coverage footprint (fixed & dynamic buffers)
- Underserved population map (~565,000 people)
- 8 high-priority clusters + 20 ranked candidate tower sites
- Interactive Folium map & static visualization
- Full MCDA scoring (pop served, tower distance, road access, slope, land use)

## Methodology
1. **Data Sources** — OpenCelliD towers, WorldPop 2020 (100 m), ESA WorldCover 2021 (10 m), OSM roads, DEM
2. **Coverage Modeling** — 2 km fixed + range-based dynamic buffers → dissolved unions
3. **Demand Mapping** — Underserved population raster (outside coverage)
4. **Clustering** — DBSCAN on high-density underserved pixels → filtered clusters ≥5,000 pop
5. **MCDA Scoring** — Weighted: pop served (40%), dist to tower (25%), dist to road (15%), slope penalty (10%), land use penalty
6. **Visualization** — Matplotlib static map + Folium interactive HTML

## Results
- **Underserved population**: ~564,832 (10.7% of 5.295 million)
- **Clusters identified**: 8 (after filtering)
- **Top candidates**: Ranked by full MCDA score (see `top_tower_candidates_full_mcda.geojson`)

## Interactive Map
Open: [`top_candidates_interactive_full.html`](top_candidates_interactive_full.html)  
(zoom, click markers for pop served, distances, slope, land use, score)

## How to Run
1. Clone repo
2. Install dependencies: `pip install -r requirements.txt`
3. Run `notebooks/Telecom_Accra_Optimization.ipynb`
