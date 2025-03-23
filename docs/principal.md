# Página principal

Modificar el archivo **index.html** para crear la página principal de la aplicación

Copiar lo siguiente

``` html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Guia Sant Boi</title>
</head>
<body>
    
</body>
</html>
``` 

Agregar la librerias externas jQuery y jQuery Mobile junto con sus css

``` html hl_lines="9 10 11 12 13"
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
    
</body>
</html>
``` 

Agregar el contenedor principal de la página

``` html hl_lines="15 16 17"
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
        
    </div>
</body>
</html>
``` 

Agregar la cabecera de la página

``` html hl_lines="16 17 18 19 20 21 22 23 24"
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

    </div>
</body>
</html>
```

Agregar el footer de la página

``` html hl_lines="25 26 27 28 29 30 31 32 33"
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

    </div>
</body>
</html>
```
