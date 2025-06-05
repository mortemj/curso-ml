# 🚀 Fase 1: Introducción a la Ciencia de Datos y Machine Learning - Los Cimientos

---

## 🎯 Objetivo de Esta Fase

Esta primera fase está diseñada para **desmitificar el Machine Learning (ML)** y construir una base sólida para tu viaje en la ciencia de datos. Nuestro objetivo principal es que comprendas qué es el ML, cómo funciona a un nivel intuitivo y por qué es una herramienta tan poderosa en la actualidad.

Al finalizar esta fase, serás capaz de:
* Identificar ejemplos de Machine Learning en tu vida cotidiana.
* Distinguir entre los principales tipos de Machine Learning (supervisado, no supervisado).
* Comprender el concepto de **clasificación binaria**, el foco de nuestro curso.
* Familiarizarte con el entorno de trabajo: **Python y Jupyter Notebooks**.
* Realizar la **carga y primera inspección** de un dataset real.
* Identificar la variable objetivo y las características en un problema de Machine Learning.

---

## 💻 Herramientas Esenciales

Para seguir esta fase, necesitarás tener acceso a las siguientes herramientas:

* **Python:** El lenguaje de programación que utilizaremos para todas nuestras tareas de Machine Learning.
* **Pandas:** Una librería de Python fundamental para la manipulación y análisis de datos.
* **Jupyter Notebooks / Google Colab:** Entornos interactivos que te permitirán escribir y ejecutar código Python de forma sencilla, visualizar resultados al instante y combinar código con texto explicativo. Si no tienes Jupyter instalado, **Google Colab** es una excelente alternativa gratuita basada en la nube que solo requiere una cuenta de Google.

---

## ✅ Prerrequisitos / Conocimientos Previos

Este curso está diseñado para ser accesible a **principiantes absolutos en Machine Learning**.

* **Conocimientos de Programación:** No se requieren conocimientos previos de programación. La sección `Recursos_Python_Jupyter.md` y los notebooks están diseñados para guiarte desde cero en lo esencial de Python.
* **Conocimientos Matemáticos/Estadísticos:** No se requieren conocimientos avanzados. Los conceptos matemáticos y estadísticos se introducirán de forma intuitiva y se explicarán en la **`Guía_Conceptos_ML.pdf`** cuando sea necesario.

---

## 📚 Materiales Incluidos en Esta Fase (¡Orden de Estudio Recomendado!)

Esta fase se compone de los siguientes archivos y recursos, diseñados para ofrecer una experiencia de aprendizaje completa y flexible. Se presentan en el orden que te sugerimos para un estudio óptimo:

1.  **`README.md` (Este Archivo):**
    * **Propósito:** Sirve como tu guía inicial para la fase, explicando los objetivos, los materiales disponibles, las herramientas utilizadas y una propuesta de cómo abordar el estudio de esta sección.

2.  **`Recursos_Python_Jupyter.md` (Archivo Markdown):**
    * **Propósito:** Una **guía rápida y práctica para principiantes** en Python y Jupyter Notebooks. Contiene comandos básicos de Python que necesitarás en el curso, así como instrucciones sobre cómo usar las celdas de un notebook, guardarlo y ejecutarlo. Incluye enlaces útiles a recursos externos.
    * [Accede a `Recursos_Python_Jupyter.md` aquí](./Recursos_Python_Jupyter.md)

3.  **`Intro_ML.ipynb` (Jupyter Notebook):**
    * **Propósito:** Este notebook te sumergirá en el mundo del Machine Learning a través de **ejemplos cotidianos y analogías intuitivas**. Definiremos formalmente el ML y exploraremos sus tipos principales, con un enfoque en la clasificación binaria. Incluye un pequeño ejercicio práctico en Python para que tengas tu primer contacto.
    * [Accede a `Intro_ML.ipynb` aquí](./Intro_ML.ipynb)

4.  **`Titanic_Dataset.ipynb` (Jupyter Notebook):**
    * **Propósito:** Aprenderás a cargar y realizar la **primera exploración de un dataset real y clásico**: el dataset del Titanic. Usaremos las funciones esenciales de Pandas (`.head()`, `.info()`, `.shape()`, `.describe()`) para entender la estructura de los datos, identificar la variable objetivo (`Survived`) y las características clave, y empezar a visualizar patrones iniciales.
    * [Accede a `Titanic_Dataset.ipynb` aquí](./Titanic_Dataset.ipynb)

5.  **`Guía_Conceptos_ML.pdf` (Documento PDF):**
    * **Propósito:** Para aquellos que prefieren una aproximación más teórica o desean consolidar los fundamentos, este documento ofrece una **explicación esencial y concisa de los conceptos teóricos** detrás del Machine Learning. Incluye definiciones clave y una explicación intuitiva de los algoritmos de aprendizaje supervisado y no supervisado.
    * [Accede directamente a la `Guía_Conceptos_ML.pdf` aquí](./Guía_Conceptos_ML.pdf)

---

## 🗺️ Cómo Usar Este Material (Paso a Paso)

Te sugiero seguir este camino para obtener el máximo provecho de la Fase 1:

1.  **Explora este `README.md`:** Ya lo estás haciendo. ¡Excelente!
2.  **Guía Rápida de Herramientas:** Si eres nuevo/a en Python o Jupyter Notebooks, te recomiendo empezar por **`Recursos_Python_Jupyter.md`**. Familiarízate con lo básico de estos entornos.
3.  **Conceptos Fundamentales (Intuitivo):** Dirígete a **`Intro_ML.ipynb`**. Este notebook te dará una comprensión práctica e intuitiva de qué es el Machine Learning a través de ejemplos cotidianos. Intenta ejecutar el pequeño ejercicio práctico en Python que se incluye.
4.  **Primer Contacto con Datos Reales:** Continúa con **`Titanic_Dataset.ipynb`**. Aquí aprenderás a cargar y explorar un dataset real, identificando sus componentes clave.
5.  **Profundiza en la Teoría:** Una vez que tengas una visión general práctica, puedes consolidar tus conocimientos con la **`Guía_Conceptos_ML.pdf`**. Este documento te ayudará a formalizar las ideas que ya habrás visto en los notebooks.
6.  **¡Practica!** No hay mejor forma de aprender que haciendo. Experimenta con los códigos, cambia valores, haz preguntas.

---

## 🔗 Relación entre los Ficheros de la Fase

Para que te hagas una idea clara de cómo se complementan los materiales de esta fase, aquí tienes un esquema simplificado de su interconexión:

```mermaid
graph TD
    A[README.md] --> E(Recursos_Python_Jupyter.md);
    A --> B(Intro_ML.ipynb);
    A --> C(Titanic_Dataset.ipynb);
    A --> D(Guía_Conceptos_ML.pdf);
    E --> M(Comandos Básicos de Python);
    E --> N(Uso de Jupyter/Colab);
    B --> F(Ejemplos Cotidianos de ML);
    B --> G(Definición y Tipos de ML);
    B --> H(Tu Primer Contacto con Python - Clasificación Sencilla);
    C --> I(Carga y Exploración Inicial);
    C --> J(Variables Objetivo y Características);
    D --> K(Teoría Esencial de ML);
    D --> L(Algoritmos Supervisados/No Supervisados - Intuitivo);
    B --- D;
    C --- D;
    B --- E;
    C --- E;
