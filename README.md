# ArcMap-to-R

The purpose of this repository is help me remember how to perform various geoprocessing operations across Esri's ArcMap and R's `sf` and `raster` packages. Sometimes the tools use the same name, sometimes they don't.

# Vector (feature class) Operations

**Operation**|**ArcMap**|**sf**| 
:-----:|:-----:|:-----:|:-----:
Project New Coordinate System|Define Projection|`st\_transform`, `st\_crs`| 
Buffer|Buffer|`st\_buffer`| 
Find Centroid|Field Calculator|`st\_centroid`| 
Simplify Geometry|Simplify Polygon, Simplify Line|`st\_simplify`| 
Triangulate Points|Create TIN|`st\_triangulate`| 
Create Voronoi Polygons|Create Theissen Polygons|`st\_voronoi`| 
Create Convex Hull|Minimum Bounding Geometry|`st\_convex\_hull`| 
Find Intersection|Intersect|`st\_intersect`| 
Find Overlap|Identity|`st\_difference`| 
Crop/Clip|Clip|`st\_crop`, `st\_intersection`| 
Spatial Join|Spatial Join|`st\_union`, `st\_join`| 
Calculate Proximity|Near|`st\_nearest\_feature`, `st\_nearest\_point`| 
Symmetrical Difference|Symmetrical Difference|`st\_sym\_difference`| 

# Raster Operations

**Operation**|**ArcMap**|**raster**
:-----:|:-----:|:-----:
Manipulate Raster Values|Raster Math|`values(r) <- {function}`, `calc`, `overlay`
Vector to Raster|Polygon to Raster|`rasterize`
Extract Values by Point|Extract Multi Values to Points|`extract`
Project CRS|Project|`crs`, `projectRaster`
Change grid cell size|Environment Settings > Raster Analysis|`aggregate`
Reclassify Values|Reclassify|`reclassify`
Hillshade|Hillshade|`hillShade`
Create contours|Contour|`contour`
Zonal statistics|Zonal Statistics, Zonal Statistics as Table|`zonal`
Aspect/Direction|Aspect|`direction`
