A lo largo de esta asignatura hemos realizado 5 proyectos individuales:

- Entrega 01:

CATEGORÍAS GRAMATICALES Y EXTRACCIÓN DE ENTIDADES 

El objetivo de esta práctica ha sido realizar un notebook en Python que realice un análisis morfológico y extraiga las entidades que se presenten en un texto. Las entidades para extraer serán de tipo organización, localización y persona. Para realizar esta actividad se ha utilizado dos sistemas ya entrenados, el entrenamiento en NLTK y en uno modelo de lenguaje de spaCy.

- Entrega 02:

CLASIFICACIÓN DE TEXTOS

Se ha realizado una clasificación de una serie de opiniones sobre un hotel, que están recogidas en el fichero hotel.csv. Este fichero contiene dos columnas. La primera, bajo el título text, contiene las opiniones a clasificar, mientras que la segunda, bajo el título label, contiene la puntuación otorgada. Las opiniones se agrupan según su calificación en un valor 5 y otro valor 3. 

En primer lugar, he realizado el preprocesamiento necesario mediante las funciones contenidas en la librería NLTK, realizando una escritura modular del código para comprobar si se obtienen mejores resultados al utilizar stop-words, al realizar una extracción de formas canónicas, etc.

En segundo lugar, he dividido el conjunto de documentos en un subconjunto de entrenamiento y otro de evaluación.

A continuación, he convertido el corpus de documentos en una matriz TF-idf, para ello he utilizado el vectorizador TfidfVectorizer, que forma parte de sklearn.

Por último, he realizado  modelos de entrenamiento con algoritmos de clasificador bayesiano ingenuo y máquinas SVM. He obtenido resultados de precisión de la clasificación, así como las matrices de confusión para ambos modelos.

Despues del trabajo realizado podemos concluir que el modelo con mejor accuracy es el de SVM con los datos transformados mediante WordNet Lemmatizer con un 71,66%. Consideramos el método Snowball Stemmer por que muestra mejor reducción de formas canónicas de los documentos en español que WordNet Lemmatizer. Sin embargo, después de realizar la práctica, compruebó que su reducción permite a los modelos trabajar de forma más precisa que el otro metodo. También creo que se podría revisar con otros tipos de modelo como árboles de decisión.

- Entrega 03:

ELABORACIÓN DE UN ASISTENTE VIRTUAL

El objetivo de este proyecto ha sido crear un asistente virtual, utilizando para ello la herramienta Watson Assistant de IBM. Se trata de realizar un chatbot para hacer una reserva de una mesa en un restaurante. El modo de entrega ha sido una exportación a JSON de las skills utilizadas.
 
- Entregas 04 y 05:
 
Ha consistido en comprobar la utilización de Embeddings y de Transformers mediante la elaboración de unos notebooks en Python. Para ello he instalado la a librería transformersde Humming Face siguiendo las instrucciones en https://github.com/huggingface/transformers.

Posteriormente, he creado un  notebook  para  hacer  análisis  de  sentimientos (Entrega_04) y  otro  para encontrar respuestas a preguntas (Entrega_05). Dado  que  la  librería transformerses  multilingüe, he realizado el  mismo trabajo con frases en español e ingles. Podemos concluir que analizando las mismas frases en español y en ingles vemos que una frase que contenga unicamente información, en ambos idiomas se clasifica como positivo en más del 99%. Lo mismo ocurre con las frases irónicas. Pero si observamos una frase que contega una negación de un sentimiento, vemos como en español tiene un 3% más de score. Es decir, clasifica mejor en español.

