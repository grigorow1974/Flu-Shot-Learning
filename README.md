# Predicción de Vacunación contra H1N1 y Gripe Estacional

Este proyecto aborda el desafío de predecir la probabilidad de que individuos reciban vacunas contra el virus H1N1 y la gripe estacional, basándose en información sobre sus antecedentes, opiniones y comportamientos de salud. Se desarrollaron modelos de aprendizaje automático utilizando datos de la Encuesta Nacional de Gripe H1N1 de 2009 (NHFS) realizada en Estados Unidos.

---

## Contexto

La pandemia de H1N1 de 2009, comúnmente conocida como "gripe porcina", afectó a millones de personas en todo el mundo y fue responsable de entre 151,000 y 575,000 muertes durante el primer año. Una vacuna para el virus H1N1 se hizo disponible públicamente en octubre de 2009.

La Encuesta Nacional de Gripe H1N1 de 2009 fue diseñada para monitorear la cobertura de vacunación durante la temporada de gripe 2009-2010 en respuesta a esta pandemia. La población objetivo de la encuesta incluyó a todas las personas de 6 meses o más que vivían en Estados Unidos al momento de la entrevista.

---

## Objetivos

- Desarrollar modelos predictivos para determinar la probabilidad de que una persona reciba la vacuna contra H1N1 y la gripe estacional  
- Identificar los factores más influyentes en la decisión de vacunación  
- Proporcionar información que pueda guiar futuros esfuerzos de salud pública  

---

## Datos

Los datos provienen de la Encuesta Nacional de Gripe H1N1 de 2009 (NHFS) realizada entre octubre de 2009 y junio de 2010. Cada fila en el conjunto de datos representa una persona que respondió a la encuesta.

**Variables objetivo:**

- `h1n1_vaccine`: Si el encuestado recibió la vacuna contra la gripe H1N1 (0 = No; 1 = Sí)  
- `seasonal_vaccine`: Si el encuestado recibió la vacuna contra la gripe estacional (0 = No; 1 = Sí)  

**Características principales:**

- Datos demográficos: edad, educación, raza, sexo, ingresos, estado civil  
- Opiniones sobre eficacia de vacunas y riesgos de enfermedad  
- Comportamientos preventivos de salud  
- Recomendaciones médicas  
- Condiciones médicas crónicas  
- Situación de empleo y vivienda  

---

## Metodología

### Exploración y Análisis de Datos:
- Análisis de la distribución de las variables objetivo  
- Identificación de valores faltantes  
- Exploración de relaciones entre variables  

### Preprocesamiento de Datos:
- Manejo de valores faltantes mediante imputación  
- Codificación de variables categóricas  
- Escalado de características numéricas  

### Modelado y Optimización:
- Implementación de diversos algoritmos (XGBoost, Random Forest, Regresión Logística)  
- Búsqueda sistemática de hiperparámetros mediante validación cruzada  
- Evaluación de modelos utilizando área bajo la curva ROC (AUC-ROC)  

### Análisis de Características Importantes:
- Identificación de las variables más influyentes en las decisiones de vacunación  
- Visualización de la importancia de características  

---

## Resultados

### Predicción de vacunación H1N1:
- **AUC-ROC:** 0.8404 ± 0.0059  
- **Características más importantes:** recomendación del médico, nivel de preocupación por H1N1, opinión sobre eficacia de la vacuna  

### Predicción de vacunación contra gripe estacional:
- **AUC-ROC:** 0.8612 ± 0.0033  
- **Características más importantes:** opinión sobre eficacia de la vacuna, recomendación del médico, percepción de riesgo  

---

## Hallazgos Clave

- Las recomendaciones médicas son uno de los factores más influyentes en la decisión de vacunación para ambos tipos de vacunas  
- La percepción de eficacia de la vacuna está estrechamente relacionada con la probabilidad de vacunación  
- Diferentes grupos demográficos muestran patrones distintos de vacunación  
- La preocupación por los efectos secundarios de las vacunas impacta negativamente en las tasas de vacunación  

---

## Cómo Utilizar Este Repositorio

### Requisitos

- Python 3.8+  
- pandas  
- numpy  
- scikit-learn  
- xgboost  
- matplotlib  
- seaborn  

### Instalación

Clona este repositorio:

```bash
git clone https://github.com/tu_usuario/prediccion-vacunacion.git
cd prediccion-vacunacion


