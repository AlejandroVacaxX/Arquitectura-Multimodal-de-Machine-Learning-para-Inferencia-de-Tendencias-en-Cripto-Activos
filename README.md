# Predicción de Criptomonedas mediante Análisis de Sentimiento (FinBERT-LSTM)

Este repositorio contiene el código fuente de un Proyecto Terminal de Ingeniería en Computación enfocado en la predicción de movimientos de precios de criptomonedas. El sistema utiliza una arquitectura de red neuronal multimodal que integra series de tiempo financieras con análisis de sentimiento extraído de redes sociales.

## 🧠 Arquitectura del Modelo

El proyecto aborda el reto de procesar simultáneamente datos estructurados y no estructurados combinando dos arquitecturas de Deep Learning:

1. **Procesamiento de Lenguaje Natural (NLP):** Implementación de **FinBERT** (y exploración con RoBERTa) para clasificar el sentimiento (Alcista, Bajista, Neutral) de publicaciones e hilos en foros de Reddit (ej. `r/CryptoCurrency`).
2. **Análisis de Series de Tiempo:** Una red neuronal recurrente **LSTM** (Long Short-Term Memory) que procesa datos históricos de precios y volumen de transacciones, integrando el vector de características de sentimiento generado por FinBERT para predecir la tendencia del activo.

## ⚙️ Fuentes de Datos

* **Datos de Mercado (Estructurados):** APIs de mercado (Yahoo Finance / Binance API) para el historial de precios (OHLCV).
* **Datos Sociales (No Estructurados):** Extracción de texto automatizada mediante la API de Reddit (PRAW) para capturar la psicología del inversor minorista.

## 🚀 Requisitos Previos e Instalación

El proyecto está desarrollado en **Python**. Se recomienda el uso de un entorno virtual.

1. Clona el repositorio:
 
Instala las dependencias:

Bash
pip install -r requirements.txt
Configuración de Variables de Entorno:
Para ejecutar los scripts de extracción de datos, necesitas credenciales de la API de Reddit. Crea un archivo .env en la raíz del proyecto y agrega tus claves:

Fragmento de código
REDDIT_CLIENT_ID=tu_client_id_aqui
REDDIT_CLIENT_SECRET=tu_client_secret_aqui
(Nota: El archivo .env está incluido en el .gitignore por seguridad).

⚠️ Descargo de Responsabilidad
Este proyecto tiene fines estrictamente académicos y de investigación en el área de Machine Learning. No constituye asesoramiento financiero ni recomendaciones de inversión. Los mercados de criptomonedas son altamente volátiles y las predicciones generadas por los modelos no garantizan resultados en entornos de mercado reales.
