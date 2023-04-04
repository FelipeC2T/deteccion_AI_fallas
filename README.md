# Deteccion_Fallas
 Detección Automatica de fallas geologicas en datos sismicos usando Deep Learning. Al ser colaborativo parte de los comentarios van a estar escritos en inglés y parte en español o espanglish, pido disculpas por la desprolijidad.
El archivo consiste en tres códigos:
1ro: "DataGenerator": Se analiza el dataset, el cual consiste en 200 cubos de entrenamiento con sus respectivas etiquetas. Estos cubos están subidos a un drive y hay que descargarlos. Instrucciones en el readme correspondiente.
Los datos etiquetados están ya contenidos en el .zip 
2do: "TRAIN_FC": se entrena una U-Net con 200 cubos sinteticos y se prueba en validación. Se puede entrenar o hacer pruebas con los modelos ya entrenados cargando los respectivos pesos.
Hay que tener en cuenta que la U-Net que usamos es una simplificada que tiene 1,4M de parámetros, mientras que la original tiene 9M. Estan definidas como "unet" y "bigunet". Hay que elegir la correspondiente al archivo que se elija.
La función de costo es "Smoothed dice loss" la cual para 15 épocas logra una buena precisión. Para ver un resultado del entrenamiento realizado por una notebook promedio, como la que estamos usando.
Se puede usar el "History" que está subido tambien en ...
En fin, los pesos cargados estan en pretrained model. Los usados por nosotros para la U-Net pequeña son "weights.h5".
3ro: "PREDICTION_FC": que es la aplicación en datos de testeo y dato real. En la carpeta "prediction" se encuentran los detalles de el dato real y un link al drive para descargar el archivo
"gxl.dat".

