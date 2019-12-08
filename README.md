# Prueba
## Varios tutoriales
**1. Como leer desde pandas un archivo csv subido a Google Drive**

Subimos el archivo csv a Drive y pulsamos con ratón derecho - Compartir

Abajo en "Avanzado" pinchamos en "Cambiar" ---> Activado: cualquier usuario con el enlace

Después "Abrir con" el archivo csv con "Hojas de Cálculo Google"

En la barra de dirección del Navegador, se sustituye "edit#gid" por "export?format=csv&gid"

(Si le damos a Enter vemos que nos da la opción de descargar el archivo csv-> funciona)

Copiamos la dirección web de la barra de direcciones, y esa será la dirección que pondremos en:

df = pd.read_csv('https://docs.google.com/spreadsheets/d/1lScnpFtSA0YtazWWGIohe9-uD3GiiYjBzA3_DMI9yy8/export?format=csv&gid=446981189')

(por ejemplo, ese link de "data.csv" lo tengo compartido en mi Google Drive)

**2. Poner icono con enlace a Google Colab de un archivo Jupyter Notebook (ipynb) en Github**

(ver github "googlecolab/colabtools") (yo le tengo hecho un fork)

https://github.com/josealfon/colabtools/blob/master/notebooks/colab-github-demo.ipynb

En el archivo ipynb abrimos una casilla de Markdown (o lo escribimos directamente en una ya creadad de Markdown)
Escribimos

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb)

(editar este archivo README.md, para poder ver el código). 

https://mybinder.org/https://mybinder.org/

Cambiamos la dirección que enlaza al archivo ipynb a la dirección de nuestro ipynb en Google Colab

**3. Binder. Subir directorio de archivos Jupyter NB (o archivo individual ipynb)**

https://mybinder.org/

  * Lanzar un repositorio completo:
  
  "Github" -> Pegamos la dirección de Github al repositorio con los ipynb (o con carpetas, subcarpetas, archivos)--> Launch
  
  * Lanzar un archivo ipynb individual:
  
  "Github" -> Repositorio donde está el archivo
  
  "Path to a notebook file (optional)" -> Nombre del archivo (p. ej.: prueba.ipynb)--> Launch
  
  IMPORTANTE. Si queremos guardarnos el link --> Al final de la configuración, copiamos el enlace al icono con la dirección de acceso.
  
 Se pone en un Markdown de Github (como Google Colab). Lleva entre corchetes tanto el icono, como la dirección de acceso. P.ej.:
 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/josealfon/prueba/master)

 OJO!! En la plataforma Binder NO están instalados los paquetes Python que queramos importar (p. ej.: import pandas as pd). Para esto, tendremos que instalarlos primero en el archivo ipynb abierto en binder --> !pip install pandas
 
 **4. Bamboolib. He creado un repositorio a partir de la plantilla (bamboo) **
 
 https://github.com/8080labs/bamboolib_binder_template/generate
 
 y después modificado el ipynb para poner mis propios csv en la carpeta "data" y así poder cambiar el nombre cuando ejecuto el Binder del ipynb (segundo binder, y está equivocado el nombre). Importante el cambiar el "pd.read_XXX según el tipo de archivo que utilice (.parquet, .csv, .xlsx)
 
También puedo pegar el link de un archivo csv de Google Drive (poniéndolo tal como se vio en el punto 1. 
