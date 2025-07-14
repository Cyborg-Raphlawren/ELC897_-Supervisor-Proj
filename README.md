# ELC897
GEOSPATIAL ANALYSIS with QGIS


1. Create a new shapefile layer\
  1.1. set geometry type to polygon\
  1.2. give a name for the layer
3. Right click on the layer and toogle editing\
   2.1 Click on add polygon feature (Ctrl + .)\
  2.2. Add elipse from center and 2 points
5. Go to processing toolbar and find Intersection\
  3.1. Do the intersection between the circle lines and the created layer
6. Right click on the intersection layer and open attribute table\
  4.1. Enable editing mode (click on pencil)\
  4.2. Open field calculator (ctrl+i)\
    4.2.1. Output field name = x2\
    4.2.2. Field type = real and precision = 5\
    4.2.3. Expression = x(start_point($geometry))\
  4.3. Open field calculator (ctrl+i)\
    4.3.1. Output field name = y2\
    4.3.2. Field type = real and precision = 5\
    4.3.3. Expression = y(start_point($geometry))\
   4.3.4. Set the date Expression = to_date('2012-05-04')\
  4.1. Disable editing mode (click on pencil) and save
8. Click the temporary scratch layer icon to save the created intersection layer
9. Right click on the intersection layer and export the csv file
10. Open the csv and copy the x2 and y2 values to test.csv

11. For holes in the shapes
    10.1. Click preprocessing
    10.2. Vector geometry
    10.3. Multipart to singleparts
    10.4. Click on the intersection layer.

12. Export the csv for each files

Next steps
1. Create more shapes (read prophet manual to see how many points it
needs to work)
2. Use pandas to read all lines in the csvs
3. Use prophet to predict the next points


Main Project:  
For the holes in the shape, after the intersection the shapes with the radical lines, 
for eacg intersections -- seperate each breaks in the shape as independent,
Preprocessing -- Vector geometry -- Multipart to single parts 
