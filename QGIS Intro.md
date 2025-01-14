# QGIS Intro

QGIS is a free, open-source, user-friendly GIS application that we will use throughout the semester. 

- Download it from https://qgis.org/download/ and follow the installation instructions for your operating system.
- Go to https://opendata.durham.ca/ and explore the various open data offerings from the Regional Municipality of Durham. 
 - Select the "Health" category and search for "Health Neighbourhoods," which is a comprehensive dataset with public health-related metrics for each census neighbourhood in the region. One item will be a map service that can be downloaded in GeoJSON, Shapefile, and Comma-Separated Values formats. The other will be a data table that can be downloaded in the same formats. 
 - Open the map service and download it in Shapefile format. A shapefile will come in a .zip bundle, and will contain data, boundary information, and more. You can learn more about shapefiles here: https://en.wikipedia.org/wiki/Shapefile
- Open QGIS and create a New Empty Project. 
- Add an OpenStreetMap layer from XYZ Tiles in the Browser windwo.
- You should be able to simply drag your shapefile bundle into the Layers window, but you could also use Layer -> Add Layer -> New Vector Layer.
- QGIS will prompt you to transform your layer from the NAD83 coordinate reference system to WGS 84. Accept this.
- Right-click the Health Neighbourhoods layer and open the attribute table. Explore it.
