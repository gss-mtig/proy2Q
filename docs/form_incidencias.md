# Formulario incidencias

Crear el archivo **form.js** en la carpeta *js*.


Agregar el archivo form.js al archivo form.html

``` html
 <script src="js/form.js"></script>
```

Copiar lo siguiente en el archivo **form.js**

``` js
let foto;
const serverURL = "https://web-uab.000webhostapp.com/";

function saveMarker() {
    const name = $('#nom').val(); 
    const desc = $('#descrip').val(); 
    const lat = $('#text-latitud').val(); 
    const lng = $('#text-longitud').val();
    
    $.ajax({
        type: 'POST',
        url: `${serverURL}incidencia.php`,
        data: {
            x: lng, 
            y: lat,
            descripcio: desc,
            nombre: name,
            foto: foto
        },
        success: function(){
            //subirFichero();
            location.href = "list.html";
        }
    });
    
}

function getCurrentPosition() {
  //TODO tomar la posicion del GPS
}

function getCameraPicture() {
  //TOOD tomar foto camara
}
```

Simular subir foto

``` js
function loadFoto(evt) {
  const image = $('#fimg');
  const imageData = URL.createObjectURL(evt.target.files[0]);
  console.log(evt.target.files[0]);
  image.attr("src", imageData);
  image.attr("mime", evt.target.files[0].type);
  foto = evt.target.files[0].name;
  image.on('load', function() {
    URL.revokeObjectURL(image.attr('src')) // free memory
  });
}

function subirFichero() {
  const files = $("#file")[0].files;
  const fd = new FormData();
  fd.append('file',files[0]);
  $.ajax({
    type: 'POST',
    url: `${serverURL}upload.php`,
    data: fd,
    contentType: false,
    mimeType: "multipart/form-data",
    processData: false,
    success: function(){
        console.log('file uploaded');
    }
  });
}

function getCameraPicture() {
  //TOOD tomar foto camara
  subirFichero();
}
```

Crear el archivo **form.css** en la carpeta *css*

``` css
#fimg {
  height: 200px;
}
```

Agregar el archivo form.css al archivo form.html

``` html
 <link rel="stylesheet" href="css/form.css"/>
```

Agregar el campo file para subir la foto
``` html
 <input type='file' id='file' accept="image/*" onchange="loadFoto(event);" />
```

Simular coger la posicion del usuario

``` js
function getCurrentPosition() {
  //TODO tomar la posicion del GPS
  var onSuccess = function(position) {
		$('#text-latitud').val(position.coords.latitude);
		$('#text-longitud').val(position.coords.longitude);
	};

	function onError(error) {
		alert('code: ' + error.code + '\n' + 'message: ' + error.message + '\n');
	}

	navigator.geolocation.getCurrentPosition(onSuccess, onError);
}
```
