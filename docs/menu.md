# Menú

Modificar el archivo **index.html** para crear el menú de la aplicación

``` html hl_lines="35 36 37 38 39 40 41"
<!DOCTYPE html>
<html lang="es">
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
                <li><a href="contact.html" data-rel="close" data-transition="none">Contacte</a></li>
            </ul>
        </div>

    </div>
</body>
</html>
```

Hacer lo mismo en el archivo **list.html** para crear el menú de la aplicación
