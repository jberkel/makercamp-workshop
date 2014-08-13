
# General concepts

 * POI: point of interest
 * GeoJSON
 * OpenStreetMap
  * [Map features](http://wiki.openstreetmap.org/wiki/Map_Features)
  * Key/Value store / tags
 * Bounding Box

# Links

 * [overpass-turbo][]

## find ping pong tables

![berliner pumpe](images/tischtennis.jpg "typical berlin ping pong table, 20th century")


### query

```xml
<query type="node">
  <has-kv k="leisure" v="pitch"/>
  <has-kv k="sport" v="table_tennis"/>
  <bbox-query {{bbox}}/>
</query>
<print/>
```

## find drinking water

![berliner pumpe](images/berliner-pumpe.jpg "typical berlin pump, 19th century")

### query

```xml
<query type="node">
  <has-kv k="amenity" v="drinking_water"/>  
  <bbox-query {{bbox}}/>
</query>
<print/>
```


[overpass-turbo]: http://overpass-turbo.eu/
