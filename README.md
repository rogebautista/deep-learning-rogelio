# Practica Deep Learning

### Introducción
En esta practica se desarrollan 2 entregables, el primer bloque comprende el desarrollo de una red neuronal multicapa y una red neuronal convolucional.
En la segunda parte se muestra la combinación de ambas técnicas en un solo modelo.

Hay algunos archivos que superan el tamaño recomendado para Github
estos se encuentran en drive, para el caso de necesitarlos, la liga es la siguiente:

[Carpeta deep learning rogelio](https://drive.google.com/drive/folders/1ynMp6ToLKZjNRISeFk8OaEzpXSSYU-sB?usp=share_link)

Los archivos que se necesitan obtener son: 
* [images.npy](https://drive.google.com/file/d/1Q4vXGfU2p2qsJCdsNpCGJJctgOlt-Egv/view?usp=sharing)
* [trainImagesX.npy](https://drive.google.com/file/d/1-2qeMyTDDLrM11Y58zvAc-L8bhUKA8Q_/view?usp=share_link)
* [transfer_l_v2.h5](https://drive.google.com/file/d/1-VDlKE5AcD2SYQik9ccCqc7W2Y7V03M_/view?usp=share_link)

### Desarrollo

En el desarrollo se encuentran las siguientes etapas:



1. [Acondicionamiento previo](1-acondicionamiento-previo.ipynb): Aquí realizamos una primer limpieza del dataset, obtenemos las imágenes y dividimos
2. [Transformaciones Train](2-transformaciones.ipynb): Aquí realizamos el análisis para selección de caracteristicas relevantes
3. [Transformaciones para Test](2-test-transformaciones.ipynb): Aplicamos lo que se hizo en train a test
4. [Primer versión de modelo MLP](4_1_Modelo-v1.ipynb): Generamos un primer modelo, aquí experimentamos con hiperparametros e intentamos mejorar el modelo
5. [Segunda versión de modelo MLP](4_1_Modelo-v2.ipynb): Aqui, en una segunda versión realizamos un entrenamiento mas general y guardamos el modelo
6. [Modelo CNN](4_2_Modelo_1.ipynb): Aqui generamos un modelo CNN por capas, no pudimos ir experimentando mas a profundidad para calcular las capas e hiperparametros
7. [Modelo CNN 2](4_2_Modelo_2.ipynb): Aqui generamos un modelo mas general, hacemos 2 pruebas.
8. [Modelo CNN Trasnfer learning](4_2_Modelo_transfer_learning.ipynb): Aquí usamos transfer learning para generar un modelo CNN y añadimos un par de capas mas, guardamos el modelo.
9. [Modelo que combina ambos](5-combine-model.ipynb): Aqui usamos las arquitecturas de los modelos previos y entrenamos un modelo que combina ambos. Se hace el
intento de usar los modelos previos para hacer un mini transfer learning, pero no se logra el resultado esperado.

Es complejo decir cual es mejor o peor modelo, existen carencias en el análisis y la limpieza de datos, el uso de un modelo ya entrenado para hacer transfer learning 
es mucho mas efectivo, se comprobo que entrenar una CNN con las 1000 imagenes se llevó en el peor caso mas de 30Gb de la GPU y en 
algunos momentos llegó a tronar.
Al final, la selección de los modelos se ha hecho por su capacidad de generalización, el tiempo de entrenamiento y el uso de recursos computacionales, la inversión económica fue de 400 MXN.
