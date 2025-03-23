# Formulario

Modificar el archivo **form.html** para crear el formulario de reporte de incidentes

Copiar lo siguiente

``` html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
</head>
<body>
    
</body>
</html>
``` 

Agregar la librerias externas jQuery y jQuery Mobile junto con sus css

``` html hl_lines="9 10 11 12"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
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
    <title>Formulario</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

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

``` html hl_lines="16 17 18 19 20 21"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Agregar un nuevo marcador de incidencia </h1>
        </div>
   
    </div>
</body>
</html>
``` 

Agregar el cuerpo principal de la página

``` html hl_lines="22 23 24"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Agregar un nuevo marcador de incidencia </h1>
        </div>
   
        <div data-role="main" class="ui-content">

        </div>

    </div>
</body>
</html>
``` 

Agregar el footer de la página

``` html hl_lines="25 26 27 28 29 30"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Agregar un nuevo marcador de incidencia </h1>
        </div>
   
        <div data-role="main" class="ui-content">

        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>Gracias por la colaboración!</h1>
            </div>
        </div>

    </div>
</body>
</html>
``` 

Agregar el formulario para introducir datos

``` html hl_lines="23 24 25 26 27 28 29 30 31 32 33 34 35 36 37"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>Formulario</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> Agregar un nuevo marcador de incidencia </h1>
        </div>
   
        <div data-role="main" class="ui-content">
            <label for="text-basic">Nom de la incidència:</label>
            <input name="nom" id="nom" placeholder="Assigna un nom a la incidència" value="" type="text">

            <label for="textarea">Descripció:</label>
            <textarea cols="40" rows="8" name="descrip" id="descrip" placeholder="Fes una breu descripció"></textarea>

            <label for="text-basic">Latitud-Longitud:</label>
            <input name="text-latitud" pattern="[0-9]*\.[0-9]*" id="text-latitud" placeholder="Latitud" value="" type="text">
            <input name="text-longitud" pattern="[0-9]*\.[0-9]*" id="text-longitud" placeholder="Longitud" value="" type="text">
            
            <div class="center"><img id="fimg" src=""></img></div>
            
            <li><a href="javascript:getCurrentPosition()" class="ui-btn ui-btn-center ui-icon-location ui-btn-icon-bottom"> Afegir posició </a></li>
            <li><a href="#anylink" class="ui-btn ui-btn-center ui-icon-camera ui-btn-icon-bottom" onclick="getCameraPicture();"> Afegir imatge </a></li>
            <li><a href="javascript:saveMarker()" class="ui-btn ui-btn-center ui-icon-check ui-btn-icon-bottom"> Crear marcador </a></li>
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>Gracias por la colaboración!</h1>
            </div>
        </div>

    </div>
</body>
</html>
``` 
