# Capa de arboles

Agregar el json de arboles

``` html
<script src="data/arboles.js"></script>
```

Crear la capa de arboles

``` js
const arboles = L.geoJson(arboles_json);
```

Agregar la capa al control de capas en la matriz de capas overlays

``` js
  ,{
      groupName: "Medio ambiente",
      layers: {
          "Contentración arboles": arboles
      }
  }
```

Crear el tematico

``` js
function createStyle(feature) {
    return {
        fillColor: feature.properties.color,
        weight: 2,
        opacity: 1,
        color: 'white',
        fillOpacity: 0.7
    }
}

const arboles = L.geoJson(arboles_json, {
    style: createStyle
}).addTo(mapa);
```

Filtrar los que tienen cero arboles

``` js
const arboles = L.geoJson(arboles_json, {
    style: createStyle,
    filter: function (geoJsonFeature) {
        return geoJsonFeature.properties["numero-arboles"] > 10;
    }
}).addTo(mapa);
```

Mostrar el numero de arboles

``` js
const arboles = L.geoJson(arboles_json, {
    style: createStyle,
    filter: function (geoJsonFeature) {
        return geoJsonFeature.properties["numero-arboles"] > 10;
    },
    onEachFeature: function (feature, layer) {
        layer.bindPopup(function (layer) {
          return `Numero arboles: ${layer.feature.properties["numero-arboles"]}`;
        });
    }
}).addTo(mapa);
```
