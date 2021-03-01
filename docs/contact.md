# Contacto

Modificar el archivo **contact.html** para poner la información de contacto de la aplicación

Copiar lo siguiente

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
</head>
<body>
    
</body>
</html>
``` 

Agregar la librerias externas jQuery y jQuery Mobile junto con sus css

``` html hl_lines="9 10 11 12 13"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    
</body>
</html>
``` 

Agregar el contenedor principal de la página

``` html hl_lines="16 17 18"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
    </div>
</body>
</html>
``` 

Agregar la cabecera de la página

``` html hl_lines="17 18 19 20 21 22 23"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Contacte </h1>
            <a href="javascript:location.href='contact.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>
   
    </div>
</body>
</html>
``` 

Agregar el cuerpo principal de la página

``` html hl_lines="24 25 26"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Contacte </h1>
            <a href="javascript:location.href='contact.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">

        </div>
   
    </div>
</body>
</html>
``` 

Agregar el footer de la página

``` html hl_lines="27 28 29 30 31 32"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Contacte </h1>
            <a href="javascript:location.href='contact.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">

        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>Gràcies per la seva colaboració!</h1>
            </div>
        </div>
   
    </div>
</body>
</html>
``` 

Agregar la información de contacto

``` html hl_lines="25 26 27 28 29 30 31"
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Contacte</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>
	<link rel="stylesheet" href="https://unpkg.com/leaflet@1.3.1/dist/leaflet.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Contacte </h1>
            <a href="javascript:location.href='contact.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">
            <p>MOU-TExSTBOI, A.A</p>
            <p>C/Balmes, 9 Manresa</p>
            <p>08242 Barcelona</p>
            <br>
            <p>Horari d'atenció al públic 9:00h - 14:00h de dilluns a divendres</p>
            <p>622568568 </p>
            <p>moutexstboi@gmail.com</p>
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>Gràcies per la seva colaboració!</h1>
            </div>
        </div>
   
    </div>
</body>
</html>
```