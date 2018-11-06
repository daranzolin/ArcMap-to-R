# ArcMap-to-R

The purpose of this repository is help me remember how to perform various geoprocessing operations across Esri's ArcMap and R's `sf` and `raster` packages. Sometimes the tools use the same name, sometimes they don't.

# Vector (feature class) Operations

**Operation**|**ArcMap**|**sf**
:-----:|:-----:|:-----:
Project New Coordinate System|Define Projection|`st_transform`, `st_crs`
Buffer|Buffer|`st_buffer`
Find Centroid|Field Calculator|`st_centroid`
Simplify Geometry|Simplify Polygon, Simplify Line|`st_simplify`
Triangulate Points|Create TIN|`st_triangulate`
Create Voronoi Polygons|Create Theissen Polygons|`st_voronoi`
Create Convex Hull|Minimum Bounding Geometry|`st_convex_hull`
Find Intersection|Intersect|`st_intersect`
Find Overlap|Identity|`st_difference`
Crop/Clip|Clip|`st_crop`, `st_intersection`
Spatial Join|Spatial Join|`st_union`, `st_join`
Calculate Proximity|Near|`st_nearest_feature`, `st_nearest_point`
Symmetrical Difference|Symmetrical Difference|`st_sym_difference`

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
