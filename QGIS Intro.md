# 1: Introdcution to QGIS

QGIS is a free, open-source, user-friendly GIS application that we will use throughout the semester. This is a very basic map-making exercise. Our goal is to create a kind of map that I showed in my slides \- a population density “choropleth” map. A choropleth map (from the Greek choros 'area/region' and plethos 'multitude') is a type of thematic map in which a set of predefined areas (like provincial or regional boundaries) is coloured or patterned in proportion to a statistical variable that represents an aggregate summary of a characteristic within each area. Commonly used variables are population density, per-capita income, COVID cases by public health unit, etc.

- Download it from https://qgis.org/download/ and follow the installation instructions for your operating system. You can explore alternatives to QGIS here [https://alternativeto.net/software/quantum-gis/](https://alternativeto.net/software/quantum-gis/)
- Go to https://opendata.durham.ca/ and explore the various open data offerings from the Regional Municipality of Durham. 
 - Select the "Health" category and search for "Health Neighbourhoods," which is a comprehensive dataset with public health-related metrics for each census neighbourhood in the region. One item will be a map service that can be downloaded in GeoJSON, Shapefile, and Comma-Separated Values formats. The other will be a data table that can be downloaded in the same formats. 
 - Open the map service and download it in Shapefile format. A shapefile will come in a .zip bundle, and will contain data, boundary information, and more. You can learn more about shapefiles here: https://en.wikipedia.org/wiki/Shapefile
- Open QGIS and create a New Empty Project. 
- Add an OpenStreetMap layer from XYZ Tiles in the Browser windwo.
- You should be able to simply drag your shapefile bundle into the Layers window, but you could also use Layer -> Add Layer -> New Vector Layer.
- QGIS will prompt you to transform your layer from the NAD83 coordinate reference system to WGS 84. Accept this.
- Right-click the Health Neighbourhoods layer and open the attribute table. Explore it.

# 2: Data Collection

- First off, we will need to get a boundary shapefile from Stats Canada. A shapefile is a simple, nontopological geospatial vector data format for storing the geometric location and attribute information of geographic features. Geographic features in a shapefile can be represented by points, lines, or polygons (areas). We'll use this link [https://www12.statcan.gc.ca/census-recensement/2021/geo/sip-pis/boundary-limites/index2021-eng.cfm?year=21](https://www12.statcan.gc.ca/census-recensement/2021/geo/sip-pis/boundary-limites/index2021-eng.cfm?year=21)
  - Select .shp format, and pick the cartographic boundary file for provinces and territories under “administrative boundaries” (although I recommend that you check out the other shapefiles as well).
  - Download the compressed file and move it to a project folder.
- Next, we need to get population estimates taken from quarterly demographic estimates by Stats Can. We'll download from here [https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1710000901](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1710000901)
  - We only need one column, so apply the same quarter in the “From” and “To” boxes. Download as displayed, then open up in Excel or Google Sheets and clear all the garbage. Remove rows 1-11 and all rows after Nunavut. Get rid of the 5 after NWT and Nunavut. Insert a header row and name column A “province” and column B “population.” Save as .csv
  
# 3: Load and Join the Data

- Open QGIS and create a "new empty project."
- Drag the unzipped shapefile into the Layers window on the left. The geographic reference system of the shapefile and the QGIS default may not match up, so click on the bottom-right coordinate reference system icon. Search for "NAD83/ Statistics Canada Lambert EPSG:3347" and apply it.
- Drag the population .csv into the Layers window.
- Right click the layer and make sure “Toggle Editing” is on. Select “Open Attribute Table” and “Open Field Calculator” (from the toolbar). Make sure “Create a new field” is selected, enter “pop” into the Output Field Name, and then enter  "population" into the expression window on the left. Select “OK” and close the Attribute Table.
- Right click the shapefile layer and select "Open Attribute Table." Examine the table. We'll be using PRENAME. Close the attribute table.
- Right click it again and select "Properties." Go to "Joins" and then press the green add/plus button at the bottom. Make sure your join field is province and your target field is “PRENAME.” Click Ok. At the bottom, press Apply and then Ok.

# 4: Visualize

- After the join, right click your shapefile layer and check the attribute table again. You should now have a population column, which means that our polygon layer now has data that can be used for a choropleth map. Close the attribute table.
- Go to Properties and select the Symbology icon. Change the top drop-down to "Categorized," and then set the Value drop-down to the new “pop” field created earlier.
- Change the colour ramp to Viridis. Viridis is designed to be:
  - Colorful, spanning as wide a palette as possible so as to make differences easy to see,
  - Perceptually uniform, meaning that values close to each other have similar-appearing colors and values far away from each other have more different-appearing colors, consistently across the range of values,
  - Robust to colorblindness, so that the above properties hold true for people with common forms of colorblindness, as well as in grey scale printing, and
  - Pretty. Use it when you need a good colour palette\!
- Hit the Classify button at the bottom. Press Apply and Ok, and watch your map update.
- If you like, right click your layer again, go to Properties, Labels, and add Single Labels using PRENAME. Make sure to update your font size and label colour accordingly. 
