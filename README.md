# Trabajo Final  
Trabajo final de la materia "Introducción a las técnicas inteligentes de resolución de problemas de planificación, secuenciación y ejecución". Maestría en Aplicación de Información Espacial (CONAE - FAMAF)
### Este repositorio contiene:
- Notebook con el código explicado: *Notas y código.ipynb*
- Archivo Readme: *README.md*
- Imagen NDVI resultante: *ndviImage.tif*
## Introducción  
Para este trabajo se implementó un programa en Python para el cálculo de NDVI en un cuerpo de agua.  
Se implementó a partir de un archivo zipeado del recorte de la zona de estudio de una imagen satelital Landsat 8, en una fecha dada. El archivo zip contiene las bandas ópticas del sensor.
## Ejecución
La ejecución se conforma de 5 pasos:
1. **Carga de las librerías**
2. **Carga de las imágenes**  
    A partir de un archivo .zip que contiene todas la bandas del sensor se procede a su extracción
3. **Exploración de las imágenes**
   1. Lectura de metadatos (dimensiones, sistema de coordenadas de referencia).
   2. Visualización de las bandas.
   3. Histogramas de las bandas.
   4. Cálculo de outliers y enmascaramiento de los mismos
4. **Cálculo de MNDWI**
   1. A partir de las bandas 3 y 6 se construye el índice  
   Fórmula de referencia *MNDWI = (Verde – SWIR)/(Verde + SWIR)*   
   2. Construcción de máscara de valores superiores de MNDWI para recortar el área del lago.
5. **Recorte de bandas con la máscara de MNDWI**
   1. Se recortan las bandas 4 y 5 en base a la máscara de MNDWI.
6. **Cálculo de NDVI y exportación de imagen**
   1. A partir de las bandas 4 y 5 recortadas se calcula el NDVI.  
   Fórmula de referencia *NDVI = (Rojo – NIR)/(Rojo + NIR)*

Para la ejecución demo se utilizó una imagen del 14-05-2023 y se selecciónó como zona de estudio el Embalse Los Molinos. La zona de estudio corresponde a un subset espacial, en forma de cuadrilátero, que contiene el lago.
## Instalación  
Construido y ejecutado en *Python 3.11.7*
## Otras consideraciones  
### Paquetes a instalar
- numpy  
- matplotlib  
- rasterio  
- zipfile  
## Autor  
**Biol. Manuel Zeballos**