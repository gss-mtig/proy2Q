# Acerca de 

Modificar el archivo **about.html** para poner la información acerca de la aplicación

Copiar lo siguiente

``` html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>L'aplicació</title>
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
    <title>L'aplicació</title>
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
    <title>L'aplicació</title>
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

``` html hl_lines="16 17 18 19 20 21 22"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>L'aplicació</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> L'aplicació </h1>
            <a href="javascript:location.href='about.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>
   
    </div>
</body>
</html>
``` 

Agregar el cuerpo principal de la página

``` html hl_lines="23 24 25"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>L'aplicació</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> L'aplicació </h1>
            <a href="javascript:location.href='about.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">

        </div>
   
    </div>
</body>
</html>
``` 

Agregar el footer de la página

``` html hl_lines="26 27 28 29 30 31"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>L'aplicació</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> L'aplicació </h1>
            <a href="javascript:location.href='about.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">

        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>MOU-TE!</h1>
            </div>
        </div>
   
    </div>
</body>
</html>
```

Agregar la información de la aplicación

``` html hl_lines="24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="format-detection" content="telephone=no" />
    <meta name="msapplication-tap-highlight" content="no" />
    <meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width" />
    <title>L'aplicació</title>
    <link rel="stylesheet" href="css/jquery.mobile-1.4.5.min.css"/>

    <script src="js/jquery-2.2.4.min.js"></script>
	<script src="js/jquery.mobile-1.4.5.min.js"></script>
</head>
<body>
    <div data-role="page">
        
        <div data-role="header" data-position="fixed">
            <a href="javascript:location.href='index.html'" data-transition="slidefade" data-direction="reverse" id=ondeviceready data-role="button" data-icon="location" data-iconpos="notext" >INDEX</a>
            <h1> L'aplicació </h1>
            <a href="javascript:location.href='about.html'" data-transition="slideup" class="ui-btn ui-icon-refresh ui-btn-corner-all ui-btn-icon-notext"></a>
        </div>

        <div data-role="main" class="ui-content">
            <div data-role="collapsible">
                <h4>Qui som?</h4>
                <p>MOU-TExSTBOI és un projecte acadèmic que permet posar en pràctica els coneixements adquirits durant el segon quadrimestre del Màster en Geoinformació</p>
            </div>
            <div data-role="collapsible">
                <h4>Objectius de l'aplicació</h4>
                <p>Tenir informació continua i de forma instantània de l’entorn urbà que s’habita i/o
                es gestiona és essencial per una major eficiència a l’hora de fer intervencions, 
                planificar el territori o realitzar tasques quotidianes entre d’altres. Disposar de les
                dades geoespacials digitalitzades ens permet mantenir aquestes actualitzades. Poder-ne 
                disposar en un entorn web i  aplicació mòbil suposa visualitzar i obtenir la informació
                desitjada al moment i per tant és possible una presa de decisions més ràpida. </p>
            </div>
            <div data-role="collapsible">
                <h4>Bases legals</h4>
                <p>- Llei de protecció de dades:</p>
                <p>- Propietat intel·lectual i Llei de Marques:</p>
                <p>- Llei de patents:</p>
                <p>- Llicència d'ús i condicions:</p>
                <p>- Llei de serveis de la societat de la informació i comerç electrònic:</p>
            </div>
            <div data-role="collapsible">
                <h4>Control de qualitat</h4>
                <p> Es garanteix una informació constantment actualitzada, un funcionament d'un 95% del temps amb una resposta àgil.</p>
            </div>
        </div>

        <div data-role="footer" data-position="fixed">
            <div data-role="footer" style="text-align:center;">
            <h1>MOU-TE!</h1>
            </div>
        </div>
   
    </div>
</body>
</html>
```