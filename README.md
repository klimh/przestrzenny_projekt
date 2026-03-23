# Spatial Analytics: Gas Station Location Optimization (Warsaw Region)

## Project Overview
This project provides a data-driven approach to identifying optimal locations for new gas stations. Using **spatial analysis** and **grid-based modeling**, the tool evaluates the geographical landscape of the Warsaw region to find "market gaps" where high demand meets low competition.

The core of the project is a **Suitability Scoring Algorithm** that ranks potential locations based on multiple spatial factors.

## Tech Stack
* **Language:** Python 3.x
* **Core Analytics:** `Pandas`, `NumPy`
* **Geospatial Processing:** `GeoPandas`, `Shapely`
* **Visualization:** `Folium` (Interactive Maps), `Matplotlib`, `Seaborn`
* **Environment:** Jupyter Notebook

## How It Works (The Methodology)
The analysis follows a multi-step pipeline to transform raw coordinates into business insights:

1. **Data Grid Generation:** The target area (Warsaw and surroundings or any other) is divided into a high-resolution grid of potential coordinates.
2. **Competitor Mapping:** Existing gas stations are mapped using coordinates to establish the current market saturation.
3. **Suitability Scoring (The Algorithm):**
   * **Competition Penalty:** Scores decrease for cells located in close proximity to existing stations (using Euclidean or Haversine distance).
   * **Demand Reward:** Scores increase for areas with higher predicted traffic or population density (based on proxy indicators).
   * **Weight Balancing:** A weighted sum is used to calculate the final "Suitability Score" for every grid cell.
4. **Interactive Visualization:** Results are rendered on an interactive map using `Folium`, allowing users to explore the best-ranked "hotspots."

## Key Insights from the Notebook
* **Identifying "Cold Spots":** The model successfully pinpointed areas where current infrastructure is insufficient compared to the estimated traffic flow.
* **Optimization:** By adjusting the weight parameters, the model can be tailored for different business strategies (e.g., aggressive expansion vs. safe positioning).

## Future Improvements
* Integration of real-time traffic data via API (e.g., TomTom or Google Maps).
* Implementation of a Voronoi diagram to better visualize "territory" ownership for each station.
* Adding socio-economic data (average income, car ownership per district).

---
*Created as a part of my portfolio in Data Science and Spatial Analytics.*
