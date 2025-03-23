# Ajustes varios


## Lista incidencias

Cambiar la URL para cargar la foto y agregar una imagen de respaldo (fallback)

``` js
<img width="200px" src="${serverURL}/photo.php?foto=${data[i].foto}" 
onerror="this.onerror=null; this.src='./img/no-image.jpeg';"
/>
```

## Formulario

Generer un nombre para el archivo de imagen

``` js
function generarNombreArchivo() {
  const nombreAleatorio = Date.now() + '-' + Math.floor(Math.random() * 10000); 
  return `${nombreAleatorio}`;
}
```

Obtener imagen en base64 y obtener el tipo de imagen

``` js
function getBase64Image(img_capt) {
  var canvas = document.createElement("canvas");
  canvas.width = img_capt.naturalWidth;
  canvas.height = img_capt.naturalHeight;
  var ctx = canvas.getContext("2d");
  ctx.drawImage(img_capt, 0, 0);
  var dataURL = canvas.toDataURL("image/png");
  return dataURL;
}

function obtenerExtensionBase64(base64) {
  const match = base64.match(/^data:image\/(png|jpeg|jpg|gif|webp|bmp);base64,/);
  return match ? match[1] : null; // Retorna la extensión o null si no coincide
}
```

Actualizar la funcion de subir fichero y subir la foto al servidor

``` js
function saveMarker() {
  const name = $('#nom').val(); 
  const desc = $('#descrip').val(); 
  const lat = $('#text-latitud').val(); 
  const lng = $('#text-longitud').val();
  const imge = getBase64Image(document.getElementById('fimg'));
  const ext = obtenerExtensionBase64(imge);
  const fotoName = generarNombreArchivo();
  $.ajax({
      type: 'POST',
      url: `${serverURL}/incidencia.php`,
      data: {
          x: lng, 
          y: lat,
          descripcio: desc,
          nombre: name,
          foto: `${fotoName}.${ext}`
      },
      success: function(){
        subirFoto(imge, fotoName)
      }
  });
}

function subirFoto(foto, name) {
  const fd = new FormData();
  fd.append('foto',foto);
  fd.append('name',name);
  $.ajax({
    type: 'POST',
    url: `${serverURL}/upload-photo.php`,
    data: fd,
    contentType: false,
    mimeType: "multipart/form-data",
    processData: false,
    success: function(){
      console.log('file uploaded');
      location.href = "list.html";
    }
  });
}
```
