# Prueba
## Varios tutoriales
1. Como leer desde pandas un archivo csv subido a Google Drive

Subimos el archivo csv a Drive y pulsamos con ratón derecho - Compartir

Abajo en "Avanzado" pinchamos en "Cambiar" ---> Activado: cualquier usuario con el enlace

Después "Abrir con" el archivo csv con "Hojas de Cálculo Google"

En la barra de dirección del Navegador, se sustituye "edit#gid" por "export?format=csv&gid"

(Si le damos a Enter vemos que nos da la opción de descargar el archivo csv-> funciona)

Copiamos la dirección web de la barra de direcciones, y esa será la dirección que pondremos en:

df = pd.read_csv('https://docs.google.com/spreadsheets/d/1lScnpFtSA0YtazWWGIohe9-uD3GiiYjBzA3_DMI9yy8/export?format=csv&gid=446981189')
(por ejemplo, ese link de "data.csv" lo tengo compartido en mi Google Drive)

2. Poner icono con enlace a Google Colab de un archivo Jupyter Notebook (ipynb) en Github

(ver github "googlecolab/colabtools") (yo le tengo hecho un fork)

https://github.com/josealfon/colabtools/blob/master/notebooks/colab-github-demo.ipynb

En el archivo ipynb abrimos una casilla de Markdown (o lo escribimos directamente en una ya creadad de Markdown)
Escribimos

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb)

(editar este archivo README.md, para poder ver el código). Cambiamos la dirección que enlaza al archivo ipynb a la dirección de nuestro ipynb en Google Colab

3. Subir directorio de archivos Jupyter NB (o archivo individual ipynb)

https://mybinder.org/

  * Lanzar un repositorio completo:
  
  "Github" -> Pegamos la dirección de Github al repositorio con los ipynb (o con carpetas, subcarpetas, archivos)--> Launch
  
  * Lanzar un archivo ipynb individual:
  
  "Github" -> Repositorio donde está el archivo
  
  "Path to a notebook file (optional)" -> Nombre del archivo (p. ej.: prueba.ipynb)--> Launch
