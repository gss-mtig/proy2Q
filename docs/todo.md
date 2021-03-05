# TODO Mapa

Agregar el document ready

``` js
$(document).ready(function() {



});
```

Agregar el control de capas

``` html
 <link rel="stylesheet" href="css/styledLayerControl.css"/>

 <script src="js/styledLayerControl.js"></script>
```

``` js
//Capas
const baseMaps = [
    {
        groupName: "Mapes base",
        layers: {
            "OpenStreetMap": osm,
            "Ortofoto": serveiOrtoCache,
            "Topogràfic": serveiTopoCache
        }
    }
];

const serveis = [
    {
        groupName: "Portals",
        layers: {
            "Portals": portals
        }
    }
];

const options = {
    container_width: "200px",
    container_maxHeight: "850px", 
    group_maxHeight: "80px",
    exclusive: false
};
const controlLayers = new L.Control.styledLayerControl(baseMaps, serveis, options);
mapa.addControl(controlLayers);
```

Agregar el font-awesome

``` html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"/>
``` 

Agregar el control de localizacion

``` html
<link rel="stylesheet" href="css/L.Control.Locate.min.css"/>

<script src="js/L.Control.Locate.min.js"></script>
``` 

``` js
//leaflet control geolocalizacion
L.control.locate({drawCircle:false}).addTo(mapa);
```

Agregar el control de medida

``` html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/gokertanrisever/leaflet-ruler@master/src/leaflet-ruler.css" crossorigin="anonymous">  

<script src="https://cdn.jsdelivr.net/gh/gokertanrisever/leaflet-ruler@master/src/leaflet-ruler.js" crossorigin="anonymous"></script>
```

``` js
//Medida
L.control.ruler({
	position: 'topleft'
}).addTo(mapa);
``` 

Agregar la vista de calle

```html
<script type="text/javascript" src="http://maps.googleapis.com/maps/api/js?key=[TU_API_KEY]"></script>
``` 

``` css
#panorama {
    position:absolute;
    z-index:1000;	
    left: 10px;
    bottom: 100px;
    height:150px;
    width:200px;
    resize: both;
    background-color:transparent !important;
}
```

``` js
// en el search control descomentar
//streetView(latlng.lat, latlng.lng)

//leaflet Street View
function streetView(lat,lng){
    document.getElementById("panorama").style.visibility = 'visible';
    panorama = new google.maps.StreetViewPanorama(
        document.getElementById('panorama'), {
        position: {lat: lat , lng: lng},
        pov: {heading: 290, pitch: 10},
        zoom: 1
    });
    panorama.setOptions({
        addressControl: false,
        panControl: false,
        enableCloseButton: true
    });
}

mapa.on("contextmenu", function(evento){
    var coordenada= evento.latlng;
    streetView(coordenada.lat, coordenada.lng)
});
```

Agregar el resto de capas geojson al mapa

``` html
<script src="data/farmacies.js"></script>
<script src="data/aparcament.js"></script>
<script src="data/BBVA.js"></script>
.....
```

``` js
//Farmacies
const icono_farmacia = L.icon({
    iconUrl: 'iconos/farmacia.png',
    iconSize: [16,16]
});
const farmacies = L.Proj.geoJson(farmacies_json,{
    'pointToLayer': function (feature,latlng){
        return L.marker(latlng,{icon:icono_farmacia});
    }
})

//Aparcaments
const icono_aparcament = L.icon({
    iconUrl: 'iconos/aparcament.png',
    iconSize: [16,16]
});
const aparcament = L.Proj.geoJson(aparcament_json,{
    'pointToLayer': function (feature,latlng){
        return L.marker(latlng,{icon:icono_aparcament});
    }
})

//BBVA
const icono_BBVA = L.icon({
    iconUrl: 'iconos/BBVA.png',
    iconSize: [16,16]
});
const BBVA = L.Proj.geoJson(BBVA_json,{
    'pointToLayer': function (feature,latlng){
        return L.marker(latlng,{icon:icono_BBVA});
    }
})
.....
```

Modificar el control del capas

``` js
const serveis = [
    { 
        groupName : "Entitats bancàries",
        layers    : {
            "BBVA" :  BBVA,
            "CaixaBank"  :  caixabanc,
            "Santander"   :  santander,
            "Sabadell" : sabadell
        }
    }, {
        groupName : "Sanitat",
        layers    : {
            "Hospital" : hospital,
            "CAP" : CAP,
            "Farmacies" : farmacies
        }
    }, {
        groupName : "Educació",
        layers    : {
            "Escoles" : escoles,
            "Biblioteques"      : biblio
        }
    }, {
        groupName : "Oci i lleure",
        layers    : {
            "Parcs" : parcs,
            "Poliesportius"      : poliesport,
            "Oci"      : oci,
            "Restaurants" : restaurant
        }
    }, {
        groupName : "Consum",
        layers    : {
            //"Supermercats" : supermercats,
            "Alcampo" : alcampo,
            "BonArea" : bonarea,
            "Condis" : condis,
            "Caprabo" : caprabo,
            "Consum" : consum,
            "Dia" : dia,
            "Mercadona" : mercadona
        }
    }, {
        groupName : "Serveis",
        layers    : {
            //"Serveis Públics" : serveispublics,
            "Ajuntament" : ajuntament,
            "DNI" : DNI,
            "Museu" : museu,
            "Policia" : policia,
            "Serveis socials" : serveissocials,
            "Tanatori" : tanatori,
            "Parades bus"      : paradesbus,
            "Aparcament" : aparcament,
            "Gasolineres" : gasolineres,
            "Ferrocarrils" : ferrocarrils
        }
    }, {
        groupName : "Portals",
        layers    : {
            "Portals" : portals
        }
    } 								
];

```

