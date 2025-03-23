# Proyecto 2do Quatrimestre

[https://gss-mtig.github.io/proy2Q/](https://gss-mtig.github.io/proy2Q/)

## Temario

## Entorno

Se puede crear un entorno para generar la documentación instalando [venv](https://docs.python.org/3/library/venv.html#)

Para crear el *enviroment* abrir la consola y escribir

```bash
python3 -m venv mkdocs
```

Para activar el nuevo *enviroment* escribir

```bash
source mkdocs/bin/activate
```

También se puede crear un entorno para generar la documentación instalando [Anaconda](https://www.anaconda.com/)

Una vez instalado el Anaconda crear un *enviroment* donde instalar el mkdocs

Para crear el *enviroment* abrir la consola de Anaconda y escribir
```bash
conda create --name <NOMBRE_DEL_ENVIROMENT>
```

Para activar el nuevo *enviroment* escribir
```bash
conda activate <NOMBRE_DEL_ENVIROMENT>
```

### Herramienta de documentación

Se usa [mkdocs](http://mkdocs.org) con el tema [mkdocs-material](https://squidfunk.github.io/mkdocs-material/).

Desinstalar versiones anteriores de mkdocs:

```bash
    sudo pip uninstall mkdocs
```

E instalar con el comando:

```bash
pip install mkdocs-material
pip install mkdocs-macros-plugin
```

### Comandos mkdocs

* `mkdocs serve`: Arranca un servidor web con auto-recarga.
* `mkdocs build`: Compila la documentación en html.
* `mkdocs gh-deploy`: Publica la documentación en gh-pages.

#### Nota
    
1. git subtree split --prefix site -b gh-pages # create a local gh-pages branch containing the splitted output folder
2. git push -f origin gh-pages:gh-pages # force the push of the gh-pages branch to the remote gh-pages branch at origin
3. git branch -D gh-pages # delete the local gh-pages because you will need it: ref

Para publicar en gh-pages

1. mkdocs build
2. ghp-import site
3. git push origin gh-pages

### Layout

    mkdocs.yml    # El fichero de configuración.
    docs/
        index.md  # La portada.
        ...       # Otras páginas en markdown, imágenes, etc.

### Markdown

* Chuleta rápida sobre links, imágenes y tablas en markdown: http://www.mkdocs.org/user-guide/writing-your-docs/#linking-documents
* [Especificación Markdown](http://spec.commonmark.org/0.28/) completa.
* Visual Studio Code ofrece una vista de Preview que va mostrando el resultado del markdown en tiempo real sin tener que salir del editor.
