# ES_Neural_Network_sales_prediction

Descripción

Breve descripción del propósito y alcance del proyecto. Mencionar que se trata de un pronóstico de series temporales utilizando una red neuronal con embeddings.

An embedding involves converting a discrete, often categorical, variable into a vector of continuous numbers. In the realm of neural networks, embeddings refer to low-dimensional, learned vectors that represent discrete variables in a continuous space. The significance of neural network embeddings lies in their ability to decrease the dimensionality of categorical variables and effectively capture the essence of categories in the transformed space.
There are three main objectives for neural network embeddings:

- Identifying nearest neighbors within the embedding space, which can be utilized for generating recommendations based on user interests or clustering categories.
- Serving as input to a machine learning model for a supervised task.
- Facilitating visualization of concepts and relationships between categories.

## Requisitos del Sistema

### Flask

- Instalar Anaconda en el servidor ó en nuestra máquina local para desarrollo. (Para servidores también puedes usar la versión de mini-conda)
- Prueba ejecutar el comando “conda” en el terminal para verificar que esté todo en orden.
- Crear un nuevo environment en el que trabajaremos conda create --name mi_ambiente python=3.6
Activa el ambiente creado con source activate mi_ambiente
Instalar los paquetes Python que utilizaremos: pip install flask gunicorn

Pasos para crear la API con Flask:
A continuación está el código con el que crearemos la API y donde incorporaremos nuestro modelo. Está compuesto por los siguientes archivos:

utiles.py – Contiene funciones y utilidades comunes que son utilizadas en varios lugares dentro del proyecto.

server.py – Importa la clase Flask de la biblioteca Flask.
Define Rutas y Funciones Asociadas
Crea una instancia de la aplicación Flask.
Inicia del Servidor.
Se especifica el host y el puerto en los que se ejecutará la aplicación.

api_train_model.py – entreno y creación del modelo, una red neuronal con Embeddings.

test_api.py – Ejemplo de request POST para probar la API. Se crea un método inicial que será invocado desde la url “predict”
Cargaremos el modelo que entrenamos previamente.
Responderemos peticiones en formato JSON.

time_series.csv – Dataset.

bash
''' bash
git clone <URL_del_repositorio>
'''
cd <nombre_del_directorio>
Instalar las dependencias
pip install -r requirements.txt

python app.py
La API estará disponible en <http://localhost:5000> por defecto.
