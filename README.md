## Description
3D Hawaii map showing Maui fires using QGIS and Blender, QGIS for clipping the DEM and sateliite image, and Blender for creating the 3D terrain and then mapping the satellite image as a texture on top of it.

## Steps

### 1. Add GIS plugin
  
### 2. Import DEM

2-1 Mode
- GIS → Import → Georeferenced raster → Click on "Maui.tif"
- Mode: DEM as displacement texture (if not DEM then basemap on new plane)
- Projection: CRS WGS84

2-2 UV Map
- Click on the tool icon on the right bottom corner
- There is currently "DEM" and "DEM.001"
- For "DEM.001" set strength to 1   

2-3 View
- Click "N" to open view
- Clip-start: 0.01
- End: 1000

2-4 Set the view / zoom
- Click on "Maui" on the sidebar
- Click on the tilde sign to bring up the view menu
- Click on "View selected"

2-5 Make grid finer
- Go back to the tool icon
- "DEM" set levels-viewport to 6 and render to 6
- Click on Add modifier → Generate → Subdivision surface
- For the new subdivider → set levels-viewport to 6 and render to 5
- Drag the subdivider above the "DEM.001" and below the "DEM"

### 3. Import raster (satellite image)

3-1 Mode
- Mode: Basemap on mesh 
- node is automatically added in Shader editor
- Then can change image in Shader editor if you want

3-2 Increase height
- Then click on the map, then S, the Z, then drag to increase the height

### 4. Import shapefile (burned areas)

### 5. Import shapefiles points
- As objects
- Elevation object: Maui DEM 
- Separate objects
- Select all the points we want, then select the mesh (from SYMBOLOGY) we want to link it to
→ comm + L → link object data 





