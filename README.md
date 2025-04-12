# Script de Procesamiento de Aves 

Este repositorio contiene un script automatizado para procesar datos ornitológicos en Perú, con integración a bases de datos internacionales y oficiales.

##  Contenido del repositorio

- Descargar el archivo zip
- `script_aves.R`: Script principal.
- `/datos`: Carpeta para colocar el archivo CSV de entrada (`aves_ejemplo.csv`).
- `/Private`: Funciones auxiliares.
- `/Resultados`: Carpeta donde se guarda el archivo de salida (`aves_completo.csv`).
- `categorias_miangri2014.txt`: Listado oficial del MINAGRI (Perú).

##  Funcionalidades

- Hace match con la base `aves_peru_2025_v1` del paquete `avesperu`.
- Consulta categorías de conservación usando la API de la IUCN.
- Verifica si la especie está listada en CITES o CMS (Species+).
- Añade la categoría nacional según el Decreto Supremo MINAGRI (archivo txt alojado en GitHub).
  
##  Requisitos

- R y RStudio instalados.
- Claves API para:
  - IUCN: https://api.iucnredlist.org/users/sign_up
  - Species+: https://api.speciesplus.net/users/sign_up

##  Formato del archivo CSV

- Debe contener una columna `scientific_name` obligatoria.
- El separador debe ser `;` (puedes cambiarlo en el script).
- Si se incluye abundancia, usar la columna `ind`.

##  Instrucciones rápidas

1. Descomprime la carpeta `script_aves.zip`.
2. Abre `script_aves.R` en RStudio.
3. Cambia la ruta de trabajo (`setwd()`).
4. Reemplaza tus claves API.
5. Ejecuta todo el script (`Ctrl + A` luego `Ctrl + Enter`).
6. El resultado estará en la carpeta `/Resultados`.


 
CONTACTO: gerar.bio14@gmail.com
