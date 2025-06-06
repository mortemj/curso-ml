# 📊 Plan Detallado - Fase 2: Exploración y Limpieza de Datos (EDA)

## 🎯 Objetivo Principal de Esta Fase

El objetivo principal de esta fase es capacitarte para que puedas entender, inspeccionar y preparar cualquier dataset para su posterior uso en modelos de Machine Learning. Aprenderás a identificar problemas comunes en los datos y a aplicar técnicas efectivas para limpiarlos y transformarlos, asegurando que tus modelos trabajen con la mejor información posible.

## 🗝️ Analogía Clave de la Fase: El Detective de Datos

Imagina que eres un "detective de datos". Tu misión es examinar cuidadosamente la "escena del crimen" (tu dataset) para encontrar pistas (patrones, relaciones), identificar "sospechosos" (valores atípicos, anomalías), y limpiar cualquier "evidencia falsa o contaminada" (valores faltantes, duplicados) antes de poder resolver el caso (construir un modelo predictivo fiable).

## 🛠️ Herramientas Clave en Python

* **Pandas:** La librería fundamental para la manipulación, análisis y estructuración de datos. Será tu principal aliada.
* **Matplotlib y Seaborn:** Librerías de visualización de datos esenciales para crear gráficos informativos y entender las distribuciones y relaciones.
* **NumPy:** Base para operaciones numéricas eficientes, especialmente cuando trabajemos con arrays de datos.
* **Scikit-learn:** Aunque es conocida por el modelado, también ofrece herramientas cruciales para el preprocesamiento de datos (imputación, escalado, codificación).
* **(Opcional) Missingno:** Una pequeña librería que facilita la visualización de patrones de valores faltantes.

## 📊 Dataset Principal para la Fase 2: Melbourne Housing Snapshot

**¿Por qué este dataset?**
El dataset **Melbourne Housing Snapshot** es un conjunto de datos real y manejable que utilizaremos como ejemplo principal a lo largo de esta fase. Contiene una rica mezcla de:
* **Características Reales y Categoricas:** Permite practicar la identificación de tipos de datos.
* **Valores Faltantes:** Presenta diversos patrones de valores ausentes en varias columnas, ideal para practicar estrategias de imputación.
* **Outliers:** Contiene valores atípicos que requieren detección y manejo.
* **Relaciones Complejas:** Permite explorar correlaciones y relaciones entre variables para la detección de patrones.

Su complejidad moderada lo hace perfecto para aplicar todas las técnicas de EDA y limpieza que aprenderemos, sin ser abrumador.

---

## 📚 Módulos y Contenido Detallado de la Fase 2

### Módulo 2.1: Exploración Inicial del Dataset

**Contenido:** En este módulo, aprenderás a realizar la primera "investigación" de un dataset: cómo cargarlo, entender su estructura básica, identificar tipos de datos y obtener una visión general de sus características.

#### 1. Primer Contacto con el Dataset: Carga e Inspección Inicial

* **Cómo cargar un dataset en Python:** `pd.read_csv()`.
* **Inspección Rápida:**
    * `df.head()`, `df.tail()`, `df.sample()`: Para ver las primeras/últimas/muestras de filas.
    * `df.shape`: Dimensión (filas, columnas).
    * `df.info()`: Resumen de tipos de datos y conteo de valores no nulos.
    * `df.describe()`: Estadísticas descriptivas básicas para columnas numéricas.
    * `df.columns`: Nombres de las columnas.
    * **Identificación de Valores Únicos:** `.nunique()` para cada columna.
    * **Análisis de Valores Frecuentes:** `.value_counts()` para variables categóricas y discretas.

#### 2. Visualización de Datos para la Exploración

* **Histogramas:** Para visualizar la distribución de variables numéricas. Aprenderás a interpretar la forma, el sesgo y la presencia de múltiples modos.
* **Diagramas de Caja (Boxplots):** Esenciales para visualizar la distribución de variables numéricas, identificar la mediana, cuartiles y, crucialmente, la presencia de posibles outliers.
* **Diagramas de Dispersión (Scatter Plots):** Para explorar la relación entre dos variables numéricas, buscando correlaciones o patrones.
* **Gráficos de Barras (`countplot`):** Para visualizar la frecuencia de las categorías en variables categóricas.
* **Mapas de Calor (`heatmap`):** Para visualizar la matriz de correlación entre múltiples variables numéricas, identificando rápidamente relaciones fuertes.
* **Diagramas de Pares (`pairplot`):** Una herramienta poderosa para visualizar relaciones entre múltiples pares de variables de una vez.
* **Visualizaciones Numéricas vs. Categóricas:** Boxplots o violin plots para comparar la distribución de una variable numérica a través de las categorías de otra.

#### 3. Ejercicios Complementarios (Módulo 2.1)

* **Ejercicio 1:** Carga el dataset "Melbourne Housing Snapshot" y realiza una inspección inicial completa: `head()`, `info()`, `describe()`, `shape`.
* **Ejercicio 2:** Identifica y muestra los 5 valores más frecuentes de al menos 3 columnas categóricas (`value_counts()`).
* **Ejercicio 3:** Genera histogramas para 3 variables numéricas diferentes y boxplots para las mismas 3 variables. Interpreta sus distribuciones.
* **Ejercicio 4:** Crea un diagrama de dispersión entre 'Área de la Tierra' y 'Precio' en el dataset. ¿Observas alguna relación?
* **Ejercicio 5:** Calcula la matriz de correlación de las variables numéricas y visualízala con un `heatmap`. ¿Qué correlaciones te parecen más interesantes?
* **Ejercicio 6:** Utiliza un `boxplot` para visualizar la distribución de 'Precio' según el 'Tipo de Propiedad'.

### Módulo 2.2: Manejo de Valores Faltantes y Duplicados

**Contenido:** Una vez que hemos explorado los datos, es común encontrar "agujeros" (valores faltantes) o entradas repetidas (duplicados). Este módulo te dará las herramientas para gestionarlos.

#### 1. Detección y Tratamiento de Valores Faltantes

* **Identificación:**
    * `df.isnull()`, `df.isna()`: Para identificar valores nulos.
    * `df.isnull().sum()`: Conteo de valores faltantes por columna.
    * `df.isnull().sum() / len(df) * 100`: Porcentaje de valores faltantes por columna.
    * **Visualización de patrones de faltantes (ej. librería `missingno`)**.
* **Estrategias de Eliminación:**
    * `df.dropna(axis=0)`: Eliminación de filas con cualquier valor faltante.
    * `df.dropna(axis=1)`: Eliminación de columnas con cualquier valor faltante.
    * Discusión: ¿Cuándo eliminar filas o columnas? (Umbrales de % de faltantes).
* **Estrategias de Imputación (Relleno):**
    * **Imputación con un valor constante:** `df.fillna(valor)`.
    * **Imputación con la Media:** `.fillna(df['col'].mean())` (para variables numéricas).
    * **Imputación con la Mediana:** `.fillna(df['col'].median())` (más robusta a outliers).
    * **Imputación con la Moda:** `.fillna(df['col'].mode()[0])` (para variables categóricas o discretas).
    * **Introducción a `SimpleImputer` de Scikit-learn:** Uso de diferentes estrategias ('mean', 'median', 'most_frequent', 'constant').
    * Consideraciones sobre la imputación avanzada (ej. por regresión, K-NN Imputer, mención).

#### 2. Manejo de Valores Duplicados

* **Detección de Duplicados:**
    * `df.duplicated()`: Identifica filas completas que son duplicados.
    * `df.duplicated(subset=['col1', 'col2'])`: Identifica duplicados basados en un subconjunto de columnas.
    * `df.sum()` para contar duplicados.
* **Eliminación de Duplicados:**
    * `df.drop_duplicates()`: Elimina filas duplicadas.
    * Discusión: ¿Cuándo eliminar y qué duplicado conservar (primer/último)?

#### 3. Ejercicios Complementarios (Módulo 2.2)

* **Ejercicio 1:** Carga el dataset de Melbourne. Cuantifica los valores faltantes por columna y muestra el porcentaje. Visualízalos usando `missingno.matrix()`.
* **Ejercicio 2:** Elige una columna numérica con faltantes y rellénala con la mediana. Elige otra y rellénala con un valor constante que tenga sentido.
* **Ejercicio 3:** Elige una columna categórica con faltantes y rellénala con la moda.
* **Ejercicio 4:** Identifica y cuenta cuántas filas duplicadas exactas hay en el dataset. Elimina esas filas duplicadas.
* **Ejercicio 5:** Investiga si hay duplicados basados solo en las columnas 'Dirección' y 'Fecha de Venta'. Si los hay, elimínalos conservando la primera aparición.

### Módulo 2.3: Detección y Manejo de Outliers y Anomalías

**Contenido:** Este módulo explora cómo identificar "puntos extraños" en tus datos que podrían afectar el rendimiento de tus modelos.

#### 1. Definición y Diferencia: Outliers vs. Anomalías

* **Outliers:** Puntos de datos que se desvían significativamente de la mayoría de los otros puntos.
* **Anomalías:** Eventos raros o inusuales que no siguen el patrón esperado del resto de los datos (puede ser más amplio que un simple outlier).
* ¿Por qué es importante detectarlos? Impacto en medias, varianzas y modelos.

#### 2. Métodos de Detección de Outliers

* **Visualización:**
    * **Diagramas de Caja (Boxplots):** La herramienta visual más común. Explicación de los "bigotes" y los puntos fuera de ellos.
    * Histogramas y gráficos de densidad: Para identificar colas largas o picos inusuales.
    * Diagramas de dispersión: Para identificar puntos atípicos en relaciones entre dos variables.
* **Métodos Estadísticos:**
    * **Rango Intercuartil (IQR):** Explicación de Q1, Q3, IQR y cálculo de límites superior e inferior. Implementación en Python.
    * **Z-score:** Explicación de su uso para datos que siguen una distribución normal. Identificación de valores más allá de 2 o 3 desviaciones estándar.
    * Mención de otros métodos (Isolation Forest, Local Outlier Factor - LOF, para algoritmos de ML).

#### 3. Estrategias de Manejo de Outliers

* **Eliminación:** Cuándo es apropiado (errores de medición, errores de entrada).
* **Transformación:**
    * Transformación logarítmica (`np.log()`), raíz cuadrada, u otras transformaciones de potencia. Reducen el sesgo y el impacto de valores extremos.
* **Capping (Winsorización):** Limitar los valores de los outliers a un umbral máximo o mínimo (ej. reemplazar valores por encima del percentil 99 con el valor del percentil 99).
* **Manejo con modelos robustos:** Mención de que algunos modelos son menos sensibles a outliers.

#### 4. Ejercicios Complementarios (Módulo 2.3)

* **Ejercicio 1:** Utiliza boxplots para identificar posibles outliers en la columna 'Precio' y 'Tamaño de la Tierra' del dataset de Melbourne.
* **Ejercicio 2:** Calcula el IQR para la columna 'Precio' y define los límites superior e inferior para los outliers. ¿Cuántos outliers identificas usando este método?
* **Ejercicio 3:** Aplica una transformación logarítmica a la columna 'Precio'. Visualiza su distribución antes y después con un histograma. ¿Ha reducido el sesgo y el impacto de los outliers?
* **Ejercicio 4:** Implementa el capping (winsorización) para la columna 'Tamaño de la Tierra', limitando los valores al percentil 99. Visualiza la distribución antes y después.

### Módulo 2.4: Manejo de Variables Categóricas

**Contenido:** Los algoritmos de Machine Learning generalmente requieren entradas numéricas. Este módulo te enseñará cómo convertir variables categóricas (texto o categorías) en formatos numéricos adecuados.

#### 1. Identificación y Tipos de Variables Categóricas

* Revisión de `df.info()` y `df.select_dtypes(include='object')`.
* Entender la Cardinalidad: `.nunique()`. (Baja, media, alta cardinalidad).
* Tipos de Variables Categóricas:
    * **Nominales:** Sin orden intrínseco (ej. 'Ciudad', 'Color').
    * **Ordinales:** Con un orden o ranking (ej. 'Pequeño', 'Mediano', 'Grande').

#### 2. Técnicas de Codificación (Encoding)

* **One-Hot Encoding:**
    * Explicación detallada: Crea nuevas columnas binarias para cada categoría.
    * Uso de `pd.get_dummies()`.
    * Ventajas: No asume orden, adecuado para nominales.
    * Desventajas: Aumenta la dimensionalidad (problema de la maldición de la dimensionalidad para alta cardinalidad).
* **Label Encoding (o Ordinal Encoding):**
    * Explicación: Asigna un número entero único a cada categoría.
    * Uso de `sklearn.preprocessing.LabelEncoder` (para una columna) y `OrdinalEncoder` (para múltiples columnas, asumiendo un orden).
    * Ventajas: Reduce la dimensionalidad.
    * Desventajas: Introduce un orden artificial si la variable es nominal. Cuándo usarlo.
* **Mención de otras técnicas avanzadas:**
    * Binary Encoding (para alta cardinalidad, reduce dimensiones más que One-Hot).
    * Target Encoding (codifica categorías basándose en la media de la variable objetivo, propenso a overfitting).

#### 3. Ejercicios Complementarios (Módulo 2.4)

* **Ejercicio 1:** Identifica todas las columnas categóricas en el dataset de Melbourne. Para cada una, muestra el número de valores únicos y sus 5 valores más frecuentes.
* **Ejercicio 2:** Aplica One-Hot Encoding a la columna 'Tipo de Propiedad'. ¿Cuántas columnas nuevas se crearon?
* **Ejercicio 3:** Asumiendo que la columna 'Región' tuviera un orden (ej. 'Norte' < 'Centro' < 'Sur'), aplica Label Encoding. (Nota: esta variable es nominal, el ejercicio es solo para práctica).
* **Ejercicio 4:** Investiga la columna 'Suburbio'. ¿Sería apropiado aplicar One-Hot Encoding? ¿Por qué sí o por qué no?

### Módulo 2.5: EDA Consolidación y Caso Práctico

**Contenido:** Este es el módulo donde todo se une. Aplicarás todas las técnicas aprendidas en un flujo de trabajo integral sobre el dataset de Melbourne Housing, desde la carga hasta la preparación final.

#### 1. Flujo de Trabajo Completo de EDA y Limpieza

* **Carga del Dataset:** Carga el dataset de Melbourne Housing.
* **Inspección Inicial y Resumen:** `head()`, `info()`, `describe()`, `shape`, `nunique()`.
* **Análisis de Distribuciones y Relaciones:** Revisa las variables clave con histogramas, boxplots, scatter plots, y mapas de calor. **Detección de Patrones** a través de estas visualizaciones.
* **Gestión de Valores Faltantes:**
    * Cuantifica faltantes.
    * Aplica estrategias de imputación adecuadas para cada columna (ej. mediana para 'Precio', moda para 'Habitaciones', o eliminación si el porcentaje es muy alto y no es crítico).
    * Verifica que no queden faltantes.
* **Manejo de Duplicados:**
    * Detecta y elimina filas duplicadas.
* **Detección y Tratamiento de Outliers:**
    * Identifica outliers usando boxplots e IQR en columnas clave (ej. 'Precio', 'Tamaño de la Tierra').
    * Aplica estrategias de manejo (ej. transformación logarítmica o capping).
* **Transformación de Variables Categóricas:**
    * Identifica variables categóricas.
    * Aplica One-Hot Encoding a las variables nominales adecuadas.
    * Aplica Label Encoding si hay variables ordinales.
* **Transformaciones Finales y Escalado de Datos Numéricos:**
    * **Escalado de Datos (Normalización/Estandarización):** Explicación de por qué es importante para muchos algoritmos.
        * `MinMaxScaler` (normaliza a un rango [0,1]).
        * `StandardScaler` (estandardiza a media 0, desviación estándar 1).
    * Aplicación a las columnas numéricas relevantes.
* **Resumen del Dataset Limpio y Preprocesado:**
    * `df.info()` final para ver los tipos de datos y la ausencia de nulos.
    * `df.shape` final para ver las nuevas dimensiones.
    * Discusión sobre el estado del dataset listo para el modelado.

#### 2. Ejercicios Complementarios (Módulo 2.5)

* **Ejercicio 1:** Aplica un flujo de trabajo completo de EDA y limpieza a un dataset diferente (por ejemplo, el dataset "Boston Housing" o "California Housing" simplificado, o incluso el Titanic, pero aplicando todas las técnicas).
* **Ejercicio 2:** Documenta los pasos de tu flujo de trabajo en un Markdown dentro del notebook, explicando las decisiones que tomaste en cada paso.
* **Ejercicio 3:** Compara el `df.info()` y `df.describe()` del dataset original con el dataset final, preprocesado. ¿Qué diferencias observas?
