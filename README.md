# Análisis de Sentimientos de Tweets de Elon Musk con NLP y Redes Neuronales

Este proyecto realiza un análisis de sentimientos de los tweets de Elon Musk, utilizando técnicas de Procesamiento del Lenguaje Natural (NLP) y Redes Neuronales (específicamente, un modelo LSTM). El objetivo es comprender mejor las tendencias de sentimiento expresadas en sus tweets y explorar las relaciones entre estas tendencias y otros factores, como el número de seguidores y la fuente de los tweets.

## Resumen

El proyecto se divide en las siguientes etapas:

1.  **Obtención de Datos:** Se descarga un conjunto de datos de tweets de Elon Musk desde un archivo CSV.
2.  **Preprocesamiento de Datos:** Se realiza limpieza y preparación de los datos de texto, incluyendo eliminación de URLs, menciones, caracteres especiales y palabras vacías (stopwords), además de aplicar lematización para reducir las palabras a su forma base.
3.  **Análisis de Sentimientos:** Se utiliza VADER (Valence Aware Dictionary and sEntiment Reasoner) para clasificar el sentimiento de cada tweet como positivo, negativo o neutro.
4.  **Análisis Exploratorio de Datos (EDA):** Se generan visualizaciones gráficas para explorar y entender las tendencias de sentimiento y su relación con otros factores.
5.  **Modelado con Redes Neuronales:** Se construye y entrena una red neuronal LSTM para clasificar el sentimiento de los tweets, ofreciendo una alternativa al enfoque basado en léxico.

## Estructura del Proyecto

├── README.md             # Este archivo
├──   # Directorio para almacenar el conjunto de datos
│   └── tweets_elon_musk.csv
├──   # Directorio para scripts de Python
│   └── Olguin_Juan_Manuel_Data3_Proyecto.ipynb  # Script principal para el análisis de sentimientos

## Instrucciones de Ejecución

Debido a que este proyecto se realizó en Google Colab, te proporciono dos opciones para ejecutarlo:

**Opción 1: Ejecución en Google Colab:**

1.  Abre el archivo `Olguin_Juan_Manuel_Data3_Proyecto.ipynb` (si lo tienes como un notebook) en Google Colab.  Si solo tienes los scripts, puedes crear un nuevo notebook y copiar y pegar el código en las celdas.
2.  Sube el conjunto de datos CSV (`tweets_elon_musk.csv`) a tu espacio de trabajo en Colab.
3.  Asegúrate de que la ruta al archivo en tu script `Olguin_Juan_Manuel_Data3_Proyecto.ipynb` sea correcta (por ejemplo, `"./data/tweets_elon_musk.csv"`).
4.  Ejecuta las celdas del notebook en orden.

**Opción 2: Ejecución Local:**

1.  Asegúrate de tener Python instalado en tu sistema.
2.  Clona este repositorio a tu máquina local:

```bash
git clone <URL_del_repositorio>


## Dependencias

pandas
nltk
scikit-learn
tensorflow
matplotlib
seaborn
vaderSentiment
Resultados

**El proyecto genera los siguientes resultados, que se guardan en el directorio images/:**

1.Distribución de sentimientos: Un gráfico de barras que muestra la distribución de sentimientos (positivo, negativo, neutro) en el conjunto de datos.

2.Relación entre retweets y favoritos: Un diagrama de dispersión que muestra la relación entre el número de retweets y favoritos, coloreado por el sentimiento del tweet.

3.Influencia del usuario vs. Sentimiento promedio: Un diagrama de dispersión que muestra la relación entre el número de seguidores del usuario y el sentimiento promedio de sus tweets.

4.Distribución de sentimientos por fuente: Un gráfico de barras que muestra la distribución de sentimientos según la fuente del tweet (por ejemplo, "Twitter para iPhone", "Twitter Web App").

5.Matriz de confusión de la red neuronal: muestra los aciertos y desaciertos del modelo.

6.Historial de entrenamiento del modelo: muestra la precisión del modelo durante su entrenamiento.

**Observaciones y Limitaciones**

El análisis de sentimientos se basa en VADER, que aunque es útil, puede no capturar la sutileza del lenguaje humano (sarcasmo, ironía, etc.).
El modelo LSTM se ha simplificado para facilitar la demostración. Se pueden obtener mejores resultados con modelos más complejos y mayor ajuste de hiperparámetros.
La calidad de los resultados depende en gran medida de la calidad y representatividad del conjunto de datos.
Este proyecto está diseñado para ser reproducible, pero factores como la versión de las bibliotecas y el entorno de ejecución pueden afectar a los resultados.
