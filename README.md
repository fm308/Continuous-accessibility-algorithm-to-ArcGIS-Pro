# Continuous-accessibility-algorithm-to-ArcGIS-Pro
Python script for generating continuous accessibility surfaces in ArcGIS Pro.
The tool combines Origin–Destination Cost Matrix (Network Analyst) with Spline With Barriers (Spatial Analyst) to estimate continuous travel cost from multiple destinations across a road or pedestrian network.

The algorithm automatically adapts to the selected Travel Mode, extracting its impedance attribute (e.g., meters, minutes) and using it throughout the analysis.

Features
- OD Cost Matrix–based travel cost calculation.

- Continuous accessibility surface generation using Spline With Barriers.

- Automatic detection of cost attribute and units from the chosen Travel Mode.

- Support for multiple barrier layers (polylines and polygons).

- Optional clipping geometry.

- Works with both distance- and time-based travel modes.

- Field name generated dynamically as:
Total_[ImpedanceAttribute] (e.g., Total_Meters, Total_WalkTime).
## Requirements
- Input data must be in a projected coordinate system (metric units) for correct raster cell size.

- Avoid geographic coordinate systems (degrees).

## Usage
Run the script in ArcGIS Pro as a script tool with the following parameters:
1. Network Dataset - used for OD Cost Matrix computation.
2. Travel Mode - Selected movement profile; the algorithm retrieves its cost attribute automatically.
3. Destination Features - Points representing locations from which accessibility is calculated.
4. Interval points along network (meters) - Distance between points sampled along each network edge.
5. Barrier Layers (optional) - Polygon or polyline barriers blocking or modifying travel paths.
6. Cell size - Output raster resolution (in meters units).
7. Clipping geometry (optional) - Area used to clip the interpolated raster.
8. Output raster path - Path to the resulting continuous accessibility surface.

## Examples
- Result representing cost distance in meters on the analyzed area including barriers
![mapa moj algorytm popr](https://github.com/user-attachments/assets/27f7b457-289c-41d0-a09e-71c769ffeb5f)

- Result representing cost distance in meters on the analyzed area without barriers
![mapa moj bez barier popr](https://github.com/user-attachments/assets/09ea3f5d-fe66-4df4-9630-7c07606d9bbe)

- Result representing time distance in minutes on the analyzed area including barriers
![piaseczno mapa czas](https://github.com/user-attachments/assets/782ab4df-80ef-4bbc-a176-d634dee3b5da)

