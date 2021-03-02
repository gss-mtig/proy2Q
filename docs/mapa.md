# Mapa

Modificar el archivo **index.html** para crear el mapa de la aplicación

``` html hl_lines="26 27 28 29"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Guia Sant Boi</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page" id="mapPage" >

        <div data-role="header" data-position="fixed" >
            <a href="#index_panel" class="ui-btn ui-btn-left ui-icon-bars ui-btn-corner-all ui-btn-icon-notext"></a>
            <h1>Guia Urbana de Sant Boi</h1>
            <div class="ui-btn-right">
                <a href="javascript:location.href='index.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
                <a href="javascript:location.href='form.html'" data-transition="slideup" class="ui-btn ui-icon-plus ui-btn-corner-all ui-btn-icon-notext"></a>
            </div>
        </div>

        <div id="map-content" data-role="content">
            <div id="map"></div>			
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="navbar">
                <ul>
                    <li><a href="index.html" data-transition="none" data-icon="location" class="ui-state-persist ui-btn-active">Mapa</a></li>
                    <li><a href="javascript:location.href='list.html'" data-transition="none" data-icon="grid">Lista</a></li>
                </ul>
            </div>
        </div>

        <div data-role="panel" data-display="overlay" id="index_panel" data-theme="a">
            <h2>Menú</h2>
            <ul data-role="listview">
                <li><a href="about.html" data-rel="close" data-transition="none">Sobre l'aplicació</a></li>
                <li><a href="forum.html" data-rel="close" data-transition="none">Fòrum d'opinió</a></li>
                <li><a href="contact.html" data-rel="close" data-transition="none">Contacte</a></li>
            </ul>
        </div>

    </div>
</body>
</html>
```

Agregar la librería Leaflet.js junto con su hoja de estilo

``` html hl_lines="10 14"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Guia Sant Boi</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="css/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
    <script src="js/leaflet.js"></script>
</head>
<body>
    <div data-role="page" id="mapPage" >

        <div data-role="header" data-position="fixed" >
            <a href="#index_panel" class="ui-btn ui-btn-left ui-icon-bars ui-btn-corner-all ui-btn-icon-notext"></a>
            <h1>Guia Urbana de Sant Boi</h1>
            <div class="ui-btn-right">
                <a href="javascript:location.href='index.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
                <a href="javascript:location.href='form.html'" data-transition="slideup" class="ui-btn ui-icon-plus ui-btn-corner-all ui-btn-icon-notext"></a>
            </div>
        </div>

        <div id="map-content" data-role="content">
            <div id="map"></div>			
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="navbar">
                <ul>
                    <li><a href="index.html" data-transition="none" data-icon="location" class="ui-state-persist ui-btn-active">Mapa</a></li>
                    <li><a href="javascript:location.href='list.html'" data-transition="none" data-icon="grid">Lista</a></li>
                </ul>
            </div>
        </div>

        <div data-role="panel" data-display="overlay" id="index_panel" data-theme="a">
            <h2>Menú</h2>
            <ul data-role="listview">
                <li><a href="about.html" data-rel="close" data-transition="none">Sobre l'aplicació</a></li>
                <li><a href="forum.html" data-rel="close" data-transition="none">Fòrum d'opinió</a></li>
                <li><a href="contact.html" data-rel="close" data-transition="none">Contacte</a></li>
            </ul>
        </div>

    </div>
</body>
</html>
```

Dentro de la carpeta js y css crear un archivo llamado **mapa.js** y **mapa.css** respectivamente

Agregar estos archivos a nuestro **index.html**

``` html hl_lines="11 16"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Guia Sant Boi</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="css/leaflet.css"/>
    <link rel="stylesheet" href="css/mapa.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
    <script src="js/leaflet.js"></script>
    <script src="js/mapa.js" defer></script>
</head>
<body>
    <div data-role="page" id="mapPage" >

        <div data-role="header" data-position="fixed" >
            <a href="#index_panel" class="ui-btn ui-btn-left ui-icon-bars ui-btn-corner-all ui-btn-icon-notext"></a>
            <h1>Guia Urbana de Sant Boi</h1>
            <div class="ui-btn-right">
                <a href="javascript:location.href='index.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
                <a href="javascript:location.href='form.html'" data-transition="slideup" class="ui-btn ui-icon-plus ui-btn-corner-all ui-btn-icon-notext"></a>
            </div>
        </div>

        <div id="map-content" data-role="content">
            <div id="map"></div>			
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="navbar">
                <ul>
                    <li><a href="index.html" data-transition="none" data-icon="location" class="ui-state-persist ui-btn-active">Mapa</a></li>
                    <li><a href="javascript:location.href='list.html'" data-transition="none" data-icon="grid">Lista</a></li>
                </ul>
            </div>
        </div>

        <div data-role="panel" data-display="overlay" id="index_panel" data-theme="a">
            <h2>Menú</h2>
            <ul data-role="listview">
                <li><a href="about.html" data-rel="close" data-transition="none">Sobre l'aplicació</a></li>
                <li><a href="forum.html" data-rel="close" data-transition="none">Fòrum d'opinió</a></li>
                <li><a href="contact.html" data-rel="close" data-transition="none">Contacte</a></li>
            </ul>
        </div>

    </div>
</body>
</html>
```

Modificar el archivo **mapa.css** y copiar lo siguiente

``` css
#mapPage {
    height: 84%;
    width: 100%;
}
#map{
    height: 100%;
    width: 100%;
}

#map-content{
    height: 100%;
    width: 100%;
    padding: 0px; 
    margin: 0px;
    z-index: -1;
}
``` 

Modificar el archivo **mapa.js** y copiar lo siguiente

``` js
const mapa = L.map("map").setView([41.34,2.03],15);
setTimeout(() => {
    mapa.invalidateSize();
},100);

new L.tileLayer("http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", 
    {minZoom: 8, maxZoom: 18, attribution: "OpenStreetMap"}).addTo(mapa);
```