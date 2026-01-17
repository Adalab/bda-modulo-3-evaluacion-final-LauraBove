# Análisis del Programa de Fidelización y Actividad de Vuelos

## Descripción del proyecto
Este proyecto analiza el comportamiento de los clientes dentro de un programa de fidelización de una aerolínea, combinando información sobre la actividad de vuelos con datos demográficos y de fidelización. El objetivo es identificar patrones en la reserva de vuelos, la acumulación y canje de puntos, el valor del cliente y las características de la base de clientes mediante técnicas de análisis exploratorio, análisis estadístico y visualización de datos.

---

## Conjuntos de datos
El análisis se basa en dos conjuntos de datos:

- **Customer Flight Activity**  
  Contiene información detallada sobre la actividad de vuelo de los clientes, incluyendo número de vuelos, distancia recorrida y puntos acumulados o canjeados a lo largo del tiempo.

- **Customer Loyalty History**  
  Incluye información demográfica y de fidelización de los clientes, como tipo de tarjeta, nivel educativo, salario, fechas de alta y baja, y el valor de vida del cliente (CLV).

Ambos conjuntos de datos se integran utilizando el identificador único **Loyalty Number**.

---

## Preparación y limpieza de datos
Se llevaron a cabo las siguientes tareas para garantizar la calidad y coherencia de los datos:

- Exploración inicial de la estructura de los datos, tipos de variables y valores nulos.
- Identificación y eliminación de **registros completamente duplicados** en el conjunto de datos de actividad de vuelos.
- Verificación de que los registros repetidos por cliente y periodo temporal correspondían a observaciones válidas y no a errores de duplicación.
- Detección y tratamiento de valores inconsistentes en la variable *Salary*, corrigiendo los valores negativos mediante su valor absoluto.
- Gestión de valores nulos en *Salary* mediante imputación basada en el método **KNN**, dada la elevada proporción de valores faltantes.
- Validación del conjunto de datos final tras la unión de ambos datasets.

---

## Análisis exploratorio y estadístico
El análisis realizado incluye:

- **Estadísticas descriptivas** (media, mediana, desviación estándar, coeficiente de variación e IQR) de las principales variables numéricas.
- **Identificación de valores atípicos** mediante el método del rango intercuartílico (IQR), interpretados como comportamientos extremos pero plausibles.
- **Análisis de correlación** utilizando el coeficiente de Spearman, adecuado para variables con distribuciones asimétricas y presencia de valores extremos.
- Análisis de **variables categóricas** a través de distribuciones de frecuencia (género, nivel educativo, estado civil, tipo de tarjeta, tipo de inscripción y provincia).

---

## Visualización de datos
Se emplearon distintas visualizaciones para apoyar el análisis, entre ellas:

- Gráficos de barras para analizar la distribución mensual de vuelos y la concentración geográfica de clientes.
- Diagramas de dispersión para estudiar la relación entre distancia recorrida y puntos acumulados.
- Boxplots e histogramas para analizar distribuciones, dispersión y valores extremos de variables numéricas.
- Gráficos de sectores para representar proporciones de clientes por tipo de tarjeta y provincia.
- Gráficos de barras agrupadas para analizar la distribución de clientes por estado civil y género.
- Gráficos de barras para comparar el salario promedio según el nivel educativo.

---

## Principales conclusiones
- La actividad de vuelo de los clientes presenta una elevada heterogeneidad, con una minoría de clientes concentrando gran parte de los vuelos, la distancia recorrida y el uso de puntos.
- Existe una relación muy fuerte entre la actividad de vuelo, la distancia recorrida y la acumulación de puntos, lo que indica que el sistema de fidelización está estrechamente ligado al comportamiento de uso.
- Variables demográficas como el salario o el género muestran una relación limitada con la actividad de vuelo.
- El valor de vida del cliente (CLV) varía considerablemente entre clientes y depende de múltiples factores, no únicamente del número de vuelos realizados.
- Se observan patrones estacionales claros en la actividad de vuelo, con mayor volumen en los meses de verano y un repunte en diciembre.
- La base de clientes se concentra principalmente en las provincias con mayor densidad poblacional.

---

## Estructura del proyecto
- `datasets/` – Archivos CSV originales  
- `notebook.ipynb` – Notebook principal con el análisis  
- `README.md` – Documentación del proyecto  

---

## Cómo ejecutar el proyecto
1. Clonar o descargar el repositorio.
2. Asegurarse de tener instaladas las librerías necesarias (`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`).
3. Ejecutar el notebook de Jupyter de principio a fin.

---

## Conclusión final
Este proyecto proporciona una visión detallada del comportamiento de los clientes dentro del programa de fidelización, destacando la importancia de la actividad de vuelo como principal factor explicativo del valor del cliente. Los resultados obtenidos pueden servir como base para estrategias de segmentación, optimización del programa de fidelización y toma de decisiones basada en datos.
