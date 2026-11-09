# Instalación y entorno de desarrollo

Esta guía explica cómo preparar y previsualizar localmente la documentación de EcoRide con MkDocs Material. Se recomienda usar Visual Studio Code, que permite editar los archivos Markdown y abrir una terminal en la carpeta del proyecto.

> EcoRide es un proyecto ficticio. Los pasos de esta página preparan únicamente el sitio de documentación; no instalan ni ejecutan la aplicación móvil, el servidor Java o PostgreSQL.

## Requisitos

- Python 3 instalado.
- `pip`, incluido con las instalaciones habituales de Python.
- Visual Studio Code (recomendado, no obligatorio).

En Windows, si Python no está instalado, descárgalo desde [python.org](https://www.python.org/downloads/). Durante la instalación, activa la opción para añadir Python al `PATH`. Para este proyecto, se recomienda usar Python 3.14 o 3.13, en lugar de una versión muy reciente para la que alguna dependencia todavía no publique paquetes precompilados.

## Abrir la carpeta del proyecto

Abre la carpeta `ecoride-docs` en VSCode. También puedes entrar desde la terminal con `cd`, usando la ruta en la que hayas guardado o descomprimido el proyecto:

```bash
cd ruta/a/ecoride-docs
```

Sustituye `ruta/a/ecoride-docs` por la ubicación real. Por ejemplo, en Git Bash, una carpeta bajo Documentos podría abrirse así:

```bash
cd "/c/Users/tu_usuario/Documents/ecoride-docs"
```

La carpeta correcta contiene `mkdocs.yml` y `docs/`.

## Crear un entorno e instalar MkDocs Material

Es preferible instalar las herramientas en un entorno virtual dentro del proyecto. Así, sus dependencias quedan aisladas de otros proyectos. En Git Bash para Windows:

```bash
py -3.14 -m venv .venv
source .venv/Scripts/activate
python -m pip install --upgrade pip
python -m pip install mkdocs-material
```

Si no tienes Python 3.14 instalado y el lanzador `py` ofrece la instrucción `py install 3.14`, puedes instalarlo con ese comando y después crear el entorno. Como alternativa, usa una versión compatible que ya tengas instalada cambiando `-3.14` por ella.

En Linux o macOS, la creación y activación del entorno virtual suele ser:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install mkdocs-material
```

`mkdocs-material` instala MkDocs junto con el tema y las extensiones que utiliza esta configuración. Por eso se instala ese paquete en vez de instalar solamente `mkdocs`.

## Comprobar la instalación

Para mostrar la versión instalada:

```bash
python -m mkdocs --version
```

En Windows, Git Bash puede mostrar `Permission denied` al intentar ejecutar directamente `mkdocs --version` desde `.venv/Scripts/`. Si sucede, usa la forma `python -m mkdocs`, que ejecuta el mismo paquete a través del Python del entorno virtual.

## Servir la documentación en local

Desde la carpeta del proyecto y con `.venv` activo, inicia el servidor local:

```bash
python -m mkdocs serve
```

Cuando el terminal indique que está sirviendo en `http://127.0.0.1:8000/`, abre esa dirección en el navegador. Mientras el comando siga ejecutándose, MkDocs observará `docs/` y `mkdocs.yml`; al guardar cambios en esos archivos, reconstruirá y recargará la página.

Para detener el servidor, vuelve a la terminal y pulsa `Ctrl+C`.

## Generar el sitio estático

Para comprobar la compilación y generar la web estática en la carpeta `site/`:

```bash
python -m mkdocs build
```

La carpeta generada `site/` puede reconstruirse cuando sea necesario y no forma parte de los archivos fuente Markdown.

## Estructura del proyecto

```text
ecoride-docs/
├── mkdocs.yml
└── docs/
    ├── index.md
    ├── instalacio.md
    ├── funcionalitats.md
    ├── arquitectura.md
    └── api.md
```

`mkdocs.yml` define el título, el tema Material y el menú. La carpeta `docs/` contiene las páginas Markdown del sitio.
