
# General concepts

## POI: point of interest

 ![POI](images/poi.jpg "point of interest")

## OpenStreetMap

![OSM](images/osm_10.jpg "10 years of OpenStreetMap")

 * [Map features](http://wiki.openstreetmap.org/wiki/Map_Features)
 * Key/Value store / tags

## GeoJSON

 ```json
 {
   "type": "FeatureCollection",
   "features": [
     {
       "geometry": {
         "type": "Point",
         "coordinates": [
           13.3192854,
           52.4904865
         ]
       }
     }
   ]
 }
 ```

# Tools

 * OpenStreetMap
 * [geojson.io][]
 * [leafletjs]
 * [overpass-turbo][]
 * http://gist.github.com
 * http://bl.ocks.org/

# Examples

## find ping pong tables

![berliner pumpe](images/tischtennis.jpg "typical berlin ping pong table, 20th century")


### query

```xml
<query type="node">
  <has-kv k="leisure" v="pitch"/>
  <has-kv k="sport" v="table_tennis"/>
  <bbox-query {{bbox}}/>
</query>
<print mode="body"/>
```

## find drinking water

![berliner pumpe](images/berliner-pumpe.jpg "typical berlin pump, 19th century")

### query

```xml
<query type="node">
  <has-kv k="amenity" v="drinking_water"/>  
  <bbox-query {{bbox}}/>
</query>
<print mode="body"/>
```

[leafletjs]: http://leafletjs.com/
[geojson.io]: http://geojson.io
[overpass-turbo]: http://overpass-turbo.eu/
