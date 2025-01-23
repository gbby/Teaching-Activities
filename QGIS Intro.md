# 1: Introduction to QGIS

QGIS is a free, open-source, user-friendly GIS application that we will use throughout the semester. This is a very basic map-making exercise. Our goal is to create a kind of map that I showed in my slides \- a population density “choropleth” map. A choropleth map (from the Greek choros 'area/region' and plethos 'multitude') is a type of thematic map in which a set of predefined areas (like provincial or regional boundaries) is coloured or patterned in proportion to a statistical variable that represents an aggregate summary of a characteristic within each area. Commonly used variables are population density, per-capita income, COVID cases by public health unit, etc.

- Download it from https://qgis.org/download/ and follow the installation instructions for your operating system. You can explore alternatives to QGIS here https://alternativeto.net/software/quantum-gis/
- Go to https://opendata.durham.ca/ and explore the various open data offerings from the Regional Municipality of Durham. 
 - Select the "Health" category and search for "Health Neighbourhoods," which is a comprehensive dataset with public health-related metrics for each census neighbourhood in the region. One item will be a map service that can be downloaded in GeoJSON, Shapefile, and Comma-Separated Values formats. The other will be a data table that can be downloaded in the same formats. 
 - Open the map service and download it in Shapefile format. A shapefile will come in a .zip bundle, and will contain data, boundary information, and more. You can learn more about shapefiles here: https://en.wikipedia.org/wiki/Shapefile
- Open QGIS and create a New Empty Project. 
- Add an OpenStreetMap layer from XYZ Tiles in the Browser window.
- You should be able to simply drag your shapefile bundle into the Layers window, but you could also use Layer -> Add Layer -> New Vector Layer.
- QGIS will prompt you to transform your layer from the NAD83 coordinate reference system to WGS84. Accept this.
- Right-click the Health Neighbourhoods layer and open the attribute table. Explore it.

# 2: Data Collection

What we'll be doing now is making a choropleth map using Canadian population data. Population data is a great starting point, as most of the relevant "per capita" statistical measures we use, from crime stats to life expectancy to the unemployment rate to rates of cardiovascular disease, start with population statistics.

- First off, we will need to get a boundary shapefile from Stats Canada. A shapefile is a simple, nontopological geospatial vector data format for storing the geometric location and attribute information of geographic features. Geographic features in a shapefile can be represented by points, lines, or polygons (areas). We'll use this link https://www12.statcan.gc.ca/census-recensement/2021/geo/sip-pis/boundary-limites/index2021-eng.cfm?year=21
  - Select .shp format, and pick the cartographic boundary file for provinces and territories under "administrative boundaries" (although I recommend that you check out the other shapefiles as well).
  - Download the compressed file and move it to a project folder.
- Next, we need to get population estimates taken from quarterly demographic estimates by Stats Can. We'll download from here https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1710000901
  - We only need one column, so apply the same quarter in the "From" and "To" boxes. Download "as displayed (exluding accompanying symbols)," then open up in Excel or Google Sheets and clear all the garbage. Remove rows 1-11 and all rows after Nunavut. Get rid of the 5 after NWT and Nunavut. Insert a header row and name column A "province" and column B "population." Save as .csv
  
# 3: Load and Join the Data

- Open QGIS and create a "new empty project."
- Drag the unzipped shapefile into the Layers window on the left. The geographic reference system of the shapefile and the QGIS default may not match up, so click on the bottom-right coordinate reference system icon. Search for "NAD83/ Statistics Canada Lambert EPSG:3347" and apply it.
- Click on "Layer" in the menu bar. Add "delimited text layer." 
- Right click the shapefile layer and select "Open Attribute Table." Examine the table. We'll be using PRENAME. Close the attribute table.
- Right click it again and select "Properties." Go to "Joins" and then press the green add/plus button at the bottom. Make sure your join field is province and your target field is "PRENAME." Click Ok. At the bottom, press Apply and then Ok.

# 4: Visualize

- After the join, right click your shapefile layer and check the attribute table again. You should now have a population column, which means that our polygon layer now has data that can be used for a choropleth map. Close the attribute table.
- Go to Properties and select the Symbology icon. Change the top drop-down to "Graduated," and then set the Value drop-down to the new "population" field created earlier.
- Change the colour ramp to Viridis. Viridis is designed to be:
  - Colourful, spanning as wide a palette as possible so as to make differences easy to see,
  - Perceptually uniform, meaning that values close to each other have similar-appearing colors and values far away from each other have more different-appearing colors, consistently across the range of values,
  - Robust to colorblindness, so that the above properties hold true for people with common forms of colorblindness, as well as in grey scale printing, and
  - Pretty. Use it when you need a good colour palette\!
- Hit the Classify button at the bottom. Press Apply and Ok, and watch your map update. You may want to try to add additional classes. 
- If you like, right click your layer again, go to Properties, Labels, and add Single Labels using PRENAME. Make sure to update your font size and label colour accordingly. 

# 5: Make it Useful

To someone unfamiliar with Canadian geography, this map might be interesting - "low population in the North!" - but it doesn't really tell us much. To someone familiar with Canadian geography, population density would be a far more useful metric. In your attribute table, you have a column for land area (the area in square kilometres of the land-based portions of 2021 Census standard geographic areas). Land area is useful for calculating population density. For reference, the land area of Ontario is 892,411.76 square kilometres and the population density is 15.9 people per square kilometre. 

For one bonus point, see if you can create a new column for population density and create a new choropleth with it. What makes it different from the first one you created?
