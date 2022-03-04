# Lista incidencias

Agregar el contenedor principal

``` html
<div id="main" class="ui-content">
    
</div>
```

Agregar la tabla al contenedor

``` html
<table data-role="table" id="incList" class="ui-responsive table-stroke">
    <thead>
        <tr>
            <th data-priority="persist">Imagen</th>
            <th>Nombre</th>
            <th>Descripcion</th>
        </tr>
    </thead>
    <tbody id="incListBody">

    </tbody>
</table>
```

Crear el archivo **list.js** en la carpeta *js*.

``` js
$(document).ready(function() {

    const serverURL = "https://web-uab.000webhostapp.com/";

    function getIncidencias(){
        const list_items= [];
        $.ajax({
            type: 'POST',
            url: `${serverURL}llista.php`,
            success: function (data) {
                for (i=0; i<data.length; i++){
                    var item = `<tr>
                    <td><img width="200px" src="${serverURL}/images/${data[i].foto}"/></td>
                    <td>${data[i].nombre}</td>
                    <td>${data[i].descripcio}</td>
                    </tr>`
                    list_items.push(item);
                }
                list = list_items.join(' ');
                $('#incListBody').append(list);
                $('#incList').table("rebuild");
        }})
    }

    getIncidencias();

});
```

Agregar el archivo list.js al archivo list.html

``` html
 <script src="js/list.js"></script>
```
