# 📊 Validación de Señales Técnicas por Fundamentos

## 🧠Descripción general

Este proyecto analiza si las señales técnicas de momentum (RSI) tienen mayor validez cuando están respaldadas por un evento fundamental real, específicamente anuncios de Ganancias.

La idea central es sencilla pero potente:
- No toda señal técnica es igual. Una señal previa a un evento fundamental relevante puede reflejar información anticipada del mercado.

## 🎯Objetivo del análisis

- Evaluar si las acciones que presentan un RSI elevado (>65) el día anterior a un anuncio de Ganancias muestran una reacción significativa en el precio de cierre del día del evento.

Esto permite responder preguntas como:
- ¿El mercado “anticipa” buenas noticias vía momentum técnico?
- ¿Un RSI alto antes de ganancias indica posicionamiento informado?
- ¿Las señales técnicas ganan fuerza cuando coinciden con catalizadores fundamentales?

## 📌Lógica del enfoque

El análisis sigue tres pasos clave:
- Identificación del evento
- Se seleccionan únicamente eventos corporativos de tipo Ganancias.
- Validación técnica previa
- Se recupera el RSI del día anterior al evento.
- Se filtran solo los casos donde RSI > 65, indicando sobrecompra / fuerte optimismo.
- Reacción del mercado
- Se observa el precio de cierre del día del anuncio para evaluar el comportamiento inmediato tras el evento.

## 🧮Qué devuelve la consulta

Para cada evento válido, el resultado incluye:
- ticker_id → Acción analizada
- fecha_ganancias → Fecha del anuncio
- rsi_dia_anterior → Nivel de momentum previo
- cierre_post_evento → Precio tras la publicación
- Ordenado por RSI descendente para destacar los casos de mayor anticipación técnica.

## 💡Insight clave

- Cuando una señal técnica fuerte aparece justo antes de un evento fundamental relevante, es más probable que represente información anticipada, posicionamiento institucional o expectativas bien fundamentadas.
- Este análisis ayuda a filtrar señales técnicas “ruidosas” y enfocarse solo en aquellas que el mercado valida con hechos.

## 🧠Casos de uso

📈 Validación de estrategias de momentum + eventos

🏦 Detección de front-running previo a earnings

🧪 Backtesting de señales técnicas condicionadas por fundamentales

⚠️ Reducción de falsas señales en trading sistemático

## 🗂️Requisitos de datos

El análisis asume la existencia de las siguientes tablas:
- eventos_corporativos
- indicadores_tecnicos
- precios_diarios
- Con fechas sincronizadas y datos técnicos calculados previamente.

## 🚀Extensiones posibles

- Medir rendimiento a +3, +5 o +10 días post-evento
- Comparar contra casos con RSI bajo antes de ganancias

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
Agrupar por sector o país

Incorporar volatilidad (kurtosis / skewness) pre-evento
