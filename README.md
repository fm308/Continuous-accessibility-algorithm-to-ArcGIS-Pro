# Continuous-accessibility-algorithm-to-ArcGIS-Pro
Python script for generating continuous accessibility surfaces in ArcGIS Pro using OD Cost Matrix and Spline With Barriers.
This repository contains a Python script that generates continuous accessibility surfaces in ArcGIS Pro using:
- OD Cost Matrix (Network Analyst),
- Spline With Barriers (Spatial Analyst),
- Support for multiple barriers (polygons & polylines),
- Optional clipping geometry,
- Time or distance as cost type.

## Requirements
- Input data and project in a projected coordinate system (metric units) to ensure the cell size parameter corresponds to exact pixel dimensions.
- IMPORTANT : Avoid using geographic coordinate systems (degrees)

## Usage
Run the script in ArcGIS Pro as a script tool with parameters:
1. Network Dataset
2. Destination points
3. Interval points (optional)
4. Barrier layers (optional)
5. Cell size
6. Cost type ("Time - Fastest Path" or "Distance - Shortest Path")
7. Clipping geometry (optional)
8. Output raster path
