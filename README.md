# Telecom-X-Parte-2-Predicción de Cancelación (Churn)
Desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.


## Introducción
El objetivo de este desafío es desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios. Esto, porque La empresa quiere anticiparse al problema de la cancelación, por lo que se debe construir un pipeline robusto para esta etapa inicial de modelado.
Los Objetivos del Desafío son: 

1.-Preparar los datos para el modelado (tratamiento, codificación, normalización).

2.-Realizar análisis de correlación y selección de variables.

3.-Entrenar dos o más modelos de clasificación.

4.-Evaluar el rendimiento de los modelos con métricas.

5.-Interpretar los resultados, incluyendo la importancia de las variables.

6.-Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.

---
## Preparar los datos para el modelado 
(Tratamiento, codificación, normalización).

-Carga y exploración de datos, se importo dataset con 7267 filas y 22 columnas

-Se hizo Verificación de tipos de columnas

-Se evaluaron y eliminaron columnas que no aportan al análisis

Procesamiento de variables categóricas, numéricas y desbalanceo de clases

Variables categóricas: Se transformaron a formato numérico usando One-Hot Encoding (pd.get_dummies), para compatibilidad con modelos de ML.


Variables numéricas: Identificadas para escalado en modelos sensibles a la escala (Regresión Logística, KNN).


Desbalanceo de clases:

Proporción de clientes que cancelaron: 25.5%

Proporción de clientes activos: 74.5%

---
## Análisis de correlación y selección de variables.

Matriz de correlación

Se creó una matríz de correlación para evaluar las relaciones entre variables

Se hizo un análisis especifico entre variables: Tiempo de contrato (antiguedad) vs Cancelación y Gasto Total vs Cancelación.

Se pudo observar que: clientes con mayor antiguedad abandonan menos (correlación negativa), clientes con mayores cargos abandonan más (correlación positiva).


---
## Entrenamiento de dos o más modelos de clasificación.
Modelado

Se dividieron los datos para entrenamiento y prueba:

Se usó para Entrenamiento: 70% 

Se usó para Prueba: 30% 

Se entrenaron dos modelos :

1.- Regresión Logística 

Permite interpretar coeficientes y entender el efecto de cada variable sobre la cancelación.

2.-Random Forest 

Permite identificar la importancia de cada variable en la predicción sin asumir relaciones lineales.


---
## Evaluar rendimiento de los modelos 
Métricas de evaluación

Para la Evaluación de modelos se usaron métricas como:

-Exactitud (Accuracy)

-Precisión

-Recall

-F1-score


---
## Interpretación de los resultados

Regresión Logística:

Se identificaron los principales coeficientes más importantes (positivo → aumenta abandono, negativo → disminuye abandono):
Entre ellos:
El contrato a uno y dos años, la antiguedad del cliente y algunos serviicos hacen que disminuya la cancelación o el abandono.


Random Forest:

las  variables con mayor importancia corresponden a gasto total, antigüedad y algunos servicios.



---
## Conclusiones
principales factores que influyen en la cancelación.

1.-Tipo y duración del contrato: Un contrato de más plazo hace que disminuya la cancelación.

2.-Antigüedad del cliente: Los clientes más antiguos presentan menor riesgo de abandonar, pudiendo considerarse más leales.

3.-Gasto total y servicios contratados: A Mayor gasto y algunos servicios adicioales (Fibra óptica por ejemplo), pueden disminuir la probabilidad de cancelar.


**Se pueden considerar las siguientes estrategias para una retención de clientes:**

-Aumentar la renovación a 1 o 2 años de contrato con métodos de pago electrónico, aplicando un pequeño descuento en la cuenta o en servicios adicionales, ya que estos servicios hacen que aumente levemente la posibilidad de cancelar.

-Premiar a los clientes más antiguos con servicios de costo marginal, que les permita obtener prestaciones adicionales sin influir de manera importante en su cuenta total.

-Aumentar la percepción del valor del Servicio.


### Cómo usar el Colab
-Cargue el archivo **Telecom_X_parte_2.ipynb** en Google colab

-Suba el archivo csv datos_tratado.csv

-Replique paso a paso las secuencias de código del colab

