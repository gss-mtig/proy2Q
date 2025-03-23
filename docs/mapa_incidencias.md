# Mapa incidencias

Descargar el plugin Leaflet ajax https://github.com/calvinmetcalf/leaflet-ajax

Agregar al plugin a la carpeta js y agregarlo al index.html

``` html
<script src="js/leaflet.ajax.js"></script>
```

Cargar la capa de incidencias en el mapa

``` js
function incidencasToGeoJson(data) {
  const geoJson = {
    type: 'FeatureCollection',
    features: []
  };

  const features = data.map(item => {
    return {
      "type": "Feature",
      "properties": {
          "nombre": item.nombre,
          "descripcio": item.descripcio,
          "foto": item.foto,
          "id": item.id_incidencias,
          "fecha": item.inc_date
      },
      "geometry": {
          "type": "Point",
          "coordinates": [item.x, item.y]
      }
    };
  });
  geoJson.features = features;
  return geoJson;
}

const serverURL = "https://web-uab.000webhostapp.com";
const incidencas = L.geoJson.ajax(`${serverURL}/llista.php`,{
  middleware:function(data){
      return incidencasToGeoJson(data);
  },
  pointToLayer: function(feature, latlng){
    return L.circleMarker(latlng, {
      radius: 6,
      fillColor: "#ff0000",
      color: "#000",
      weight: 1,
      opacity: 1,
      fillOpacity: 0.8
    }).bindPopup(`<h4>${feature.properties.nombre}</h4><img width="200px" src="${serverURL}/images/${feature.properties.foto}"/>`);
  }
}).addTo(mapa);
```

