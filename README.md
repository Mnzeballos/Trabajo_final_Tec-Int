# Trabajo Final  
Trabajo final de la materia "Introducción a las técnicas inteligentes de resolución de problemas de planificación, secuenciación y ejecución". Maestría en Aplicación de Información Espacial (CONAE - FAMAF)
## Introducción  
Para este trabajo se implementó un programa en Python.  
Se implementó a partir de un archivo zipeado del recorte de la zona de estudio de una imagen satelital Landsat 8, en una fecha dada. El archivo zip contiene las bandas ópticas del sensor.

El cálculo del índice deberá realizarse sobre el area que ocupa el lago, dejando fuera el cálculo sobre el área del territorio, para lo cual deberá recortar la imagen al contorno del lago. Una posibilidad de generar un polígono vectorial mediante el índice MNDWI[2]. Sino, queda libre a usar algún otro método para enmascarar el agua. Luego calculará el índice NDVI sobre el recorte resultante la  cual no deberá contener píxeles con nubes
## Ejecución
Se utilizaron los paquetes
Para la ejecución demo se utilizó una imagen del 14-05-2023 y se selecciónó como zona de estudio el Embalse Los Molinos.
La zona de estudio corresponde a un subset espacial , en forma de cuadrilátero, que contiene el lago.
## Instalación  
Construido y ejecutado en *Python 3.11.7*
## Algunas otras consideraciones si las hubiera  
## Autor  
**Biol. Manuel Zeballos**