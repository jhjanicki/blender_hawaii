## Description
3D Hawaii map showing Maui fires using QGIS and Blender, QGIS for clipping the DEM and sateliite image, and Blender for creating the 3D terrain and then mapping the satellite image as a texture on top of it.

## Steps

1. Add GIS plugin
  
2. Import DEM

2-1 Mode
- Mode: DEM as displacement texture
- (if not DEM then basemap on new plane)
- Projection: CRS WGS84

2-2 Tool icon
- Set strength to 1   

2-3 View
- Clip-start: 0.01
- End: 1000

2-4 Make grid finer
- Add modifier: subdivision surface: simple: change it to 6 and 6
- then add another subdivier → 6 and 5
- drag it above the DEM0.01 and below the DEM

3.Import raster (satellite image)

3-1 Mode
- Mode: Basemap on mesh 
- node is automatically added in Shader editor
- Then can change image in Shader editor if you want

3-2 Increase height
- Then click on the map, then S, the Z, then drag to increase the height

4. Import shapefile (burned areas)

5. Import shapefiles points
- As objects
- Elevation object: Maui DEM 
- Separate objects
- Select all the points we want, then select the mesh (from SYMBOLOGY) we want to link it to
→ comm + L → link object data 





