# Mapa-de-Emociones

El objetivo de este proyecto es el de usar redes neuronales de tipo BERT y SOM para realizar análisis de sentimientos. Se tiene interés en el espacio topologico donde la red BERT genera embeddings, y se quiere visualizar usando la red SOM.

Se tiene una red neuronal de tipo BERT, la cual realizó fine-tuning en la tarea de clasificación de sentimientos. Aunque esta red puede tomar oraciones y asignarles su sentimiento, se tiene interés en el embedding de oraciones que puede realizar la red. Recordar que, cuando se tiene una red tipo BERT, y esta toma una oración como input, el vector asociado al token CLS puede ser usado como embedding de la oración. Por lo tanto, las redes neuronales BERT se pueden considerar como formas de vectorización de oraciones. Dado que nuestra red BERT fue entrenada en clasificación de sentimientos, esta tiene especial conocimiento en esta área. Por lo tanto, puede ser usada para realizar vectorizaciones de oraciones donde el sentimiento de la oración es crucial para hacer el embedding.

Se quiere visualizar el espacio de embeddings del BERT. Para esto, se usa una red tipo SOM. Estas redes neuronales pueden ser usadas para visualizar espacios topológicos de dimensiones altas. Se va a entrenar una SOM en el espacio de embeddings del BERT para visualizar como se distribuyen las emociones en este. Por lo tanto, lo que se busca obtener es un mapa de emociones, el cual es la representación realizada por el SOM del espacio de embeddings del BERT.

Para realizar esto, se usa un conjunto de oraciones con sentimientos. Estas se vectorizan usando el BERT, y despues se obtiene el mapa de emociones de estos vectores usando el SOM.

Obtener el mapa de emociones es de utilidad para observar como el BERT separa las emociones entre si (es lo que se espera). Es decir, se puede usar para obtener información sobre la forma de realizar embeddings del BERT. Ademas, como se ejemplifica al final del proyecto, el mapa de emociones puede ser usando para asignar emociones a oraciones no presentes en el conjunto de datos.
