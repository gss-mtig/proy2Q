# Servidor

## Hosting 

Crear la cuenta de hosting gratis en https://www.hostinger.es/hosting-gratuito o en su defecto https://www.awardspace.com/free-hosting/

Verificar el correo

Let's create some magic

Other

nombre del proyecto: proy2Quab[NOMBRE]

Copiar el password en algun lugar seguro: [CLAVE_SITIO]

Upload your site

## Crear la base de datos

Ir a la lista de tus sitios https://www.000webhost.com/members/website/list

Manage website (boton aparece al poner el cursor sobre el sitio)

Tools > Database Manager

New Database

Database name: incidentes

Database username: [USUARIODB]

Database password: [CLAVE_DB]

Una vez finalizada la creación -> Manage -> PhpMyAdmin 

Crear una tabla llamada **incidencias**

``` sql
CREATE TABLE `incidencias` (
 `id_incidencias` bigint(20) unsigned NOT NULL AUTO_INCREMENT,
 `inc_date` timestamp NULL DEFAULT current_timestamp(),
 `x` double DEFAULT NULL,
 `y` double DEFAULT NULL,
 `descripcio` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
 `nombre` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
 `foto` varchar(100) COLLATE utf8_unicode_ci DEFAULT NULL,
 PRIMARY KEY (`id_incidencias`),
 UNIQUE KEY `id_incidencias` (`id_incidencias`)
) ENGINE=InnoDB AUTO_INCREMENT=25 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci
``` 

## Archivos del servidor

Tools > File Manager -> Upload Files

Dentro de la carpeta **public_html** crear una carpeta llamada **images**

Crear los archivos del servidor

Crear un archivo llamado **llista.php** con el siguiente contenido

``` php
<?php
header("Access-Control-Allow-Origin: *");
header('Content-type: application/json; charset=utf-8');

$mysqli = new mysqli("localhost", "IDDB_USUARIODB", "CLAVE_DB", "IDDB_incidentes") or die ("No puc connectar-me");
$mysqli->set_charset("utf8");

$query = "select * from incidencias order by inc_date desc";
$result = $mysqli->query($query);

$myarray = array();
while ($row = $result->fetch_object()) {
  $myarray[] = $row;
}

echo json_encode($myarray);

$mysqli->close();
?>
```

Crear un archivo llamado **incidencia.php** con el siguiente contenido

``` php
<?php
header("Access-Control-Allow-Origin: *");
$x = $_POST['x'];
$y = $_POST['y'];
$nombre = $_POST['nombre'];
$desc = $_POST['descripcio'];
$photo = $_POST['foto'];


$mysqli = new mysqli("localhost", "IDDB_USUARIODB", "CLAVE_DB", "IDDB_incidentes") or die ("No puc connectar-me");
$mysqli->set_charset("utf8");

$query = "insert into incidencias (inc_date,x,y,descripcio,nombre,foto) values (now(),".$x.",".$y.",'".$desc."','".$nombre."','".$photo."')";
$result = $mysqli->query($query);

echo json_encode($mysqli->insert_id);

$mysqli->close();
?>
```

Crear un archivo llamado **upload.php** con el siguiente contenido

``` php
<?php
 header("Access-Control-Allow-Origin: *");
 // Directory where uploaded images are saved
 $dirname = "images/"; 
 // If uploading file
 if ($_FILES) {
    move_uploaded_file($_FILES["file"]["tmp_name"],$dirname."/".$_FILES["file"]["name"]);
 }
?>
```

Crear un archivo llamado **index.php** con el siguiente contenido

``` php
<html>
 <head>
  <title>Prueba de PHP</title>
 </head>
 <body>
 <?php 
 echo '<p>Hola Mundo</p>'; 
 
 echo 'Versión actual de PHP: ' . phpversion();
 ?>
 </body>
</html>
```

!!! note "Opcional"
    Crear un archivo llamado **photo.php** con el siguiente contenido

    ``` php
    <?php
      header("Access-Control-Allow-Origin: *");
      $x = $_GET['foto'];
      $file_out = "images/".$x; // The image to return

      if (file_exists($file_out)) {

        $image_info = getimagesize($file_out);

        //Set the content-type header as appropriate
        header('Content-Type: ' . $image_info['mime']);

        //Set the content-length header
        header('Content-Length: ' . filesize($file_out));

        //Write the image bytes to the client
        readfile($file_out);
      }
      else { // Image file not found

          header($_SERVER["SERVER_PROTOCOL"] . " 404 Not Found");

      }
    ?>
    ```

Subir los archivos php a la carpeta **public_html**

Abrir en el navegador la url de vuestra aplicación por ejemplo https://proy2qmgeouab.000webhostapp.com

