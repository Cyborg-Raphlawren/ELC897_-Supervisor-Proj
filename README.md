# DLSC804
GEOSPATIAL ANALYSIS


1. Create a new shapefile layer
  1.1. set geometry type to polygon
  1.2. give a name for the layer
2. Right click on the layer and toogle editing
  2.1. Add elipse from center and 2 points
3. Go to processing toolbar and find Intersection
  3.1. Do the intersection between the circle lines and the created layer
4. Right click on the intersection layer and open attribute table
  4.1. Enable editing mode (click on pencil)
  4.2. Open field calculator (ctrl+i)
    4.2.1. Output field name = x2
    4.2.2. Field type = real and precision = 5
    4.2.3. Expression = x($geometry)
  4.3. Open field calculator (ctrl+i)
    4.3.1. Output field name = y2
    4.3.2. Field type = real and precision = 5
    4.3.3. Expression = y($geometry)
  4.1. Disable editing mode (click on pencil) and save
5. Click the temporary scratch layer icon to save the created intersection layer
6. Right click on the intersection layer and export the csv file
7. Open the csv and copy the x2 and y2 values to test.csv

Next steps
1. Create more shapes (read prophet manual to see how many points it
needs to work)
2. Use pandas to read all lines in the csvs
3. Use prophet to predict the next points
