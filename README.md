# Deteccion de objetos en imagenes

## Introduccion
Este trabajo pretende llevar paso por paso el proceso de identificacion de objetos en imagenes utilizando la API de Tensorflow [Tensorflow Object Detection API](https://github.com/tensorflow/models/blob/master/research/object_detection/README.md). Mas específicamente vamos a identificar botellas de cerveza y su respectiva marca.

## Generación de datos
Uno de de los puntos mas importantes al momento de querer entrenar una red neuronal de cualquier tipo, es tener la cantidad adecuada de datos para los respectivos *datos de entrenamiento* y *datos de prueba*. En dado caso no se cuenten con los suficientes datos, se pueden generar datos sintéticos. En este caso se esta trabajando con imagenes que contengan botellas de cerveza, por lo tanto manipularemos imagenes de este tipo para generar muchas imagenes a partir de un conjunto relativamente pequeño.
