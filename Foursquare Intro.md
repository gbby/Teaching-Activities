# Foursquare Intro

Foursquare Studio is a comprehensive platform that lets you conduct powerful geospatial data analysis from your browser. With it, you can:
- Visualize large amounts of location data in your browser.
- Perform geospatial analytics by grouping and joining your data.
- Gain insights by filtering and correlating your location data.
- Quickly publish and share your results.
- Access it at https://studio.foursquare.com/

Here's what you'll do:
- Get the health neighbourhoods shapefile from https://opendata.durham.ca/
- Get the health neighbourhoods table from there as well, but set a filter for "Life Expectancy in Males" on INDICATORNAME and "2009-2013" on YEAR. Make sure to toggle the filters on.
- Download in .csv format.
- Load each and join in QGIS (on "MUNCIPAL_ID" "and MUNICIPAL_"), and then export to a new shapefile that can be loaded into Foursquare Studio.
- Alternatively, load each file in Foursquare Studio, select the Columns tab in the menu bar, and select join using the more options feature.
- In your new joined dataset, set your fill colour to be based on VALUE.
