# proyecto-integrador-2
Proyecto Integrador 2 semestre Maestría en Ciencia de datos EAFIT

Modelos Predictivos de Concentración de PM2.5 en la Estación El Volador, Medellín, Antioquia

Este repositorio contiene implementaciones de modelos predictivos para la concentración del contaminante PM2.5 en la estación de monitoreo de calidad del aire El Volador en Medellín, Antioquia. 

Los modelos utilizan datos históricos para predecir niveles futuros de PM2.5, facilitando la gestión de la calidad del aire y la toma de decisiones.

Miembros del Equipo:

Manuel Alejandro Andrade Franco

Jairo David Acevedo Jaramillo

Gabriel Arcangel Santiago Castañeda

Javier Ignacio Gonzalez Álvarez

Andrés Puerta González

Contenido del Repositorio:

El repositorio incluye las siguientes carpetas:

models: Contiene archivos de implementación de los modelos predictivos.

data: Almacena conjuntos de datos utilizados para el entrenamiento y la evaluación.

Modelos Disponibles:

Modelo LSTM: Modelo de Memoria a Corto y Largo Plazo (LSTM) para la predicción de PM2.5.

Hugging Face Model Hub: Enlace

Modelo RNN: Modelo de Red Neuronal Recurrente (RNN) para la predicción de PM2.5.

Hugging Face Model Hub: Enlace

Modelo ARIMA: Modelo de Media Móvil Integrada Autoregresiva (ARIMA) para la predicción de PM2.5.

Hugging Face Model Hub: Enlace

Recursos Adicionales:

Weights & Biases (WandB): 

Accede a nuestro proyecto en WandB para obtener información interactiva sobre el entrenamiento y las métricas de evaluación de los modelos.

Enlace a WandB: Calidad del Aire Medellín

Comenzar:

Para empezar a usar los modelos y explorar los datos:

Clona este repositorio en tu máquina local.

Navega a las carpetas de modelos respectivos (lstm, rnn, arima) para acceder a los detalles de implementación.

Utiliza los archivos de datos proporcionados en la carpeta data para propósitos de entrenamiento o prueba.

Consulta WandB para obtener registros detallados de experimentos y métricas de rendimiento.

Contribución:

Agradecemos las contribuciones para mejorar la precisión, eficiencia o documentación de los modelos. 

Siéntete libre de bifurcar este repositorio, realizar mejoras y enviar solicitudes de extracción.


LSTM Model for PM2.5 Prediction
Descripción
Este modelo LSTM está diseñado para predecir los niveles de PM2.5 en el Área Metropolitana del Valle de Aburrá basado en datos históricos.

Uso
El modelo puede ser utilizado para predecir PM2.5 con datos de series temporales del área mencionada. Para usar el modelo, proporciona una secuencia de valores PM2.5 de los últimos 5 días.

Datos
El modelo fue entrenado con datos históricos de PM2.5 recopilados en el Valle de Aburrá. Estos datos incluyen mediciones diarias de concentraciones de PM2.5.

Cómo usar este modelo con la API de Hugging Face
Aquí puedes incluir un ejemplo de cómo hacer una petición a la API de Hugging Face para obtener predicciones de tu modelo. Esto puede ser útil para usuarios que desean integrar tu modelo en sus aplicaciones.

import requests

API_URL = "https://api-inference.huggingface.co/models/ManCD/lstm-pm25-model"
headers = {"Authorization": "Bearer tu_token_de_Hugging_Face"}

def query(payload):
    response = requests.post(API_URL, headers=headers, json=payload)
    return response.json()

output = query({"inputs": "aquí_tus_datos_de_entrada"})
print(output)
