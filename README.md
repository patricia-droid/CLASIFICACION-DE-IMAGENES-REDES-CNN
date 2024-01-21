https://patricia-droid.github.io/CLASIFICACION-DE-IMAGENES-REDES-CNN/

Clasificación imágenes Fashion-Mnist
La base de datos que vamos a utilizar es Fashion-Mnist, que es un conjunto de imágenes de 28x28 pixeles, en escala de grises, que representan a 10 artículos de la tienda Zalando. https://github.com/zalandoresearch/fashion-mnist

Para acceder a la base de datos podemos usar la función de Keras en R llamada dataset_fashion_mnist() que se encarga de descargar los datos. Esta función nos devolverá 4 objetos que representarán las imágenes de entrenamiento, las etiquetas de entrenamiento (clase a la que corresponde), imágenes de test y las etiquetas de test.

Las imágenes de entrenamiento y test son objetos que corresponden a un array de números decimales de dimensiones 60.000x28x28 y 10.000x28x28 respectivamente. Y las etiquetas de entrenamiento y test corresponden a un array de números enteros de dimensiones 60.000 y 10.000 respectivamente.

Tendremos 60.000 imágenes en entrenamiento, con 6.000 para cada clase y 10.000 imágenes de test, con 1.000 para cada clase.

Las 10 clases son: Label Description

0 T-shirt/top (Camiseta o top). 1 Trouser/pants (Pantalones). 2 Pullover shirt (Pullover). 3 Dress (Vestido). 4 Coat (Abrigo). 5 Sandal (Sandalias). 6 Shirt (Camisa). 7 Sneaker (Zapatos deportivos). 8 Bag (Bolso o maleta) 9 Ankle boot (Botines).

El objetivo del ejercicio es realizar una Clasificación de Imágenes en la que podamos decir a que tipo de artículo pertenece la imagen, realizando las siguientes tareas:

Construir y entrenar 2 modelos con las siguientes características:
Modelo 1: Arquitectura de red Densamente Conectada de clasificación formada por: • 2 capas ocultas densamente conectadas, de 256 y 32 neuronas respectivamente • Se usará como Función de activación de capas ocultas relu • Capa de salida con el número de neuronas y función de activación adecuadas • Se usará como Optimizador rmsprop • Elige la función de pérdida y la métrica adecuadas al problema

Modelo 2: Arquitectura de Red Convolucional de clasificación formada por: • 3 capas de convolución, con 32,64 y 128 filtros respectivamente, de tamaño 3x3, el padding que no modifique el tamaño (mantenga el mismo) y activación relu • Cada capa de convolución seguida de capa de pooling de tipo maxpooling de tamaño 2x2. • Capa de aplanado • Capa de dropout con un % del 0.3 • Capa densamente conectada de 512 neuronas y activación relu • Capa de salida con el número de neuronas y función de activación adecuadas • Elige la función de pérdida y la métrica adecuadas al problema

Con el mejor modelo que seleccionemos, usar las imágenes de test, obteniendo sus predicciones y mostrando la matriz de confusión.

Visualizar 25 imágenes aleatorias de todo el test, mostrando su predicción junto con la imagen.
