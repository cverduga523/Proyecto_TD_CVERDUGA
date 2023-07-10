# Proyecto_TD_CVERDUGA
 # Proyecto 

Materia Tratamiento de Datos 


Este proyecto de clasificación de imágenes utilizando una red neuronal convolucional adaptada y optimizada con la técnica de transferencia de aprendizaje tiene como objetivo clasificar imágenes de animales en 8 clases diferentes.

El proyecto utiliza la arquitectura de red neuronal convolucional VGG16 pre-entrenada como base. La red VGG16 es conocida por su alto rendimiento en tareas de clasificación de imágenes y es ampliamente utilizada en la comunidad de aprendizaje automático.

Los pasos principales del proyecto incluyen:

Dependencias:

 El proyecto requiere Python, frameworks como Matplotlib, Scikit-learn, Numpy, TensorFlow y Keras, y Jupyter Notebook para ejecutar el código.

Entrenamiento y prueba del modelo: 


El código proporcionado debe ser ejecutado en Jupyter Notebook. 

Este código entrena y prueba el modelo utilizando imágenes de muestra clasificadas en subdirectorios según su clase.

 También se proporciona la opción de agregar imágenes propias o modificar completamente el conjunto de datos.

ImageDataGenerator: 

Se crea una instancia de la clase ImageDataGenerator, que se utiliza para generar lotes de datos de imágenes con opciones de aumento de datos, 
preprocesamiento y otras configuraciones.

.flow_from_directory(): 
Este método se llama en la instancia de ImageDataGenerator para generar el flujo de datos desde un directorio de entrenamiento específico.

Se especifica la ruta al directorio de entrenamiento, el tamaño objetivo de las imágenes, las clases a las que pertenecen las imágenes y el tamaño del lote.

Definición de la función plots(): 
Esta función se utiliza para trazar las imágenes y se utiliza dentro del código para visualizar los datos.

Utilización de la red neuronal VGG16: 

Se utiliza el modelo de red neuronal VGG16 pre-entrenado y se adapta a la tarea de clasificación de imágenes de animales.
Esto se logra ajustando los pesos de la red y agregando capas adicionales para adaptarse al problema específico.

Proceso de entrenamiento: 

Se configuran los parámetros de entrenamiento, como el optimizador, la función de pérdida y las métricas de evaluación. En este caso, se utiliza el optimizador Adam, la función de pérdida 'categorical_crossentropy' y la métrica de evaluación 'accuracy'.

Método de entrenamiento: 
Se entrena el modelo utilizando los datos de entrenamiento y validación especificados. Se especifica el número de épocas, los datos de entrenamiento y validación, y otros parámetros relacionados con el entrenamiento del modelo.


Entrene, pruebe y guarde el modelo


#def plots(ims, figsize=(20,6), rows=2, interp=False, titles=None):
Definición de una función llamada plots que toma como argumentos:
		#ims: 
		Las imágenes que se van a trazar.
		#figsize: 
		El tamaño de la figura (ancho, alto) en pulgadas. Por defecto, se establece en (20, 6).
		#rows: 
		El número de filas de subgráficos para mostrar las imágenes. Por defecto, se establece en 2.
		#interp: 
		Indicador booleano que especifica si se debe utilizar interpolación al mostrar las imágenes. Por defecto, se establece 		en False.
		#titles: 
		Una lista opcional de títulos para las imágenes. Por defecto, se establece en None.
		
#Proceso de entrenamiento del modelo, como el optimizador, la función de pérdida y las métricas de evaluación.

Se utiliza el optimizador Adam con una tasa de aprendizaje (learning rate) de 0.07. El optimizador Adam es una opción comúnmente utilizada en el entrenamiento de modelos de aprendizaje profundo.

La función de pérdida se establece en 'categorical_crossentropy'.


#Metodo de entrenamiento
Para entrenar el modelo utilizando los datos de entrenamiento y validación especificados.

En este caso, se utilizan los siguientes parámetros:#train_batches: Representa los datos de entrenamiento, que pueden ser generados por un generador de datos o simplemente un conjunto de datos de numpy.
#steps_per_epoch=1: 
Indica el número de pasos que se tomarán en cada época de entrenamiento. En este caso, se toma solo un paso, lo que 		significa que se procesa solo un lote de datos en cada época.
		#validation_data=test_batches: 
		Representa los datos de validación, que también pueden ser generados por un generador de datos o un conjunto de datos 		de numpy.
		#validation_steps=10: 
		Indica el número de pasos que se tomarán durante la evaluación del modelo en cada época de validación. En este caso, 		se toman 10 pasos, lo que significa que se evalúan 10 lotes de datos en cada época de validación.
		#epochs=20:
		Especifica el número de épocas de entrenamiento. Cada época representa una pasada completa a través de los datos de 		entrenamiento.
		#verbose=2: 
		Controla el nivel de detalle de los mensajes de registro durante el entrenamiento. Un valor de 2 muestra una barra 		de progreso por cada época y muestra información detallada sobre el progreso del entrenamiento.

