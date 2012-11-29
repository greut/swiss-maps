# Swiss Maps

This repo hosts Swiss canton and municipality geodata in open formats that can be used to build static and interactive maps (e.g. with [D3](http://d3js.org)).

Following formats are available or planned for the near future:

- [ESRI Shapefile](http://en.wikipedia.org/wiki/Shapefile)
- [GeoJSON](http://www.geojson.org/)
- [TopoJSON](https://github.com/mbostock/topojson) (soon!)

## Development Notes

### ESRI Shapefiles

The ESRI Shapefiles are generated with [QGIS](http://qgis.org) using the 'V200' municipality area Shapefiles (QGIS wouldn't combine the cantons with the 'swissBOUNDARIES3D' files). Foreign municipalities are removed. 

The CRS is set to *WGS84* because that's the default for GeoJSON.

The simplified shapefiles are generated with [MapShaper](http://mapshaper.org), using the Visvalingam algorithm with 50% simplification.

### GeoJSON

The GeoJSON files are derived directly from the shapefiles with `ogr2ogr -f geoJSON file.geojson file.shp`. The simplified versions are additionally compressed with [LilJSON](https://github.com/migurski/LilJSON).

## Copyright and License

### Author

Jeremy Stucki, [Interactive Things](http://interactivethings.com)

### Data Source

Data source is the Swiss Federal Office of Topography, [swissBOUNDARIES3D](http://www.swisstopo.admin.ch/internet/swisstopo/en/home/products/landscape/swissBOUNDARIES3D.html) 2012.

### License

This agreement under public law in accordance with Article 12, paragraph 1b of the Swiss Federal Act of 5 October 2007 on Geoinformation (hereinafter referred to as Geoinformation Act) regulates access to, and use of, the federal geodata database.

By accepting this agreement, the licensee acknowledges all contractual provisions – in particular the scope of the licence and the contractual obligations – as well the applicability of Swiss federal legislation governing geoinformation.

By accepting this agreement, the licensee also acknowledges the sole right of the licensor to regulate access to, and use of, the federal geodata database. The attention of the licensee is herewith drawn to the fact that geodata may be protected under copyright law. The licensee thus acknowledges the exclusive right of the licensor to determine the use of the data.

[Full license agreement](http://www.toposhop.admin.ch/en/shop/terms/use/finished_products)