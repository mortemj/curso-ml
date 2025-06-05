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

## 📚 Materiales Incluidos en Esta Fase

Esta fase se compone de los siguientes archivos y recursos, diseñados para ofrecer una experiencia de aprendizaje completa y flexible. Se presentan en el orden que te sugerimos para un estudio óptimo:

README.md (Este Archivo):

Propósito: Sirve como tu guía inicial para la fase, explicando los objetivos, los materiales disponibles, las herramientas utilizadas y una propuesta de cómo abordar el estudio de esta sección.
Recursos_Python_Jupyter.md (Archivo Markdown):

Propósito: Una guía rápida y práctica para principiantes en Python y Jupyter Notebooks. Contiene comandos básicos de Python que necesitarás en el curso, así como instrucciones sobre cómo usar las celdas de un notebook, guardarlo y ejecutarlo. Incluye enlaces útiles a recursos externos.
Accede a Recursos_Python_Jupyter.md aquí (Este enlace funcionará una vez que el archivo esté en la misma carpeta).
Intro_ML.ipynb (Jupyter Notebook):

Propósito: Este notebook te sumergirá en el mundo del Machine Learning a través de ejemplos cotidianos y analogías intuitivas. Definiremos formalmente el ML y exploraremos sus tipos principales, con un enfoque en la clasificación binaria. Incluye un pequeño ejercicio práctico en Python para que tengas tu primer contacto.
Accede a Intro_ML.ipynb aquí (Este enlace funcionará una vez que el archivo esté en la misma carpeta).
Titanic_Dataset.ipynb (Jupyter Notebook):

Propósito: Aprenderás a cargar y realizar la primera exploración de un dataset real y clásico: el dataset del Titanic. Usaremos las funciones esenciales de Pandas (.head(), .info(), .shape(), .describe()) para entender la estructura de los datos, identificar la variable objetivo (Survived) y las características clave, y empezar a visualizar patrones iniciales.
Accede a Titanic_Dataset.ipynb aquí (Este enlace funcionará una vez que el archivo esté en la misma carpeta).
Guía_Conceptos_ML.pdf (Documento PDF):

Propósito: Para aquellos que prefieren una aproximación más teórica o desean consolidar los fundamentos, este documento ofrece una explicación esencial y concisa de los conceptos teóricos detrás del Machine Learning. Incluye definiciones clave y una explicación intuitiva de los algoritmos de aprendizaje supervisado y no supervisado.
Accede directamente a la Guía_Conceptos_ML.pdf aquí (Este enlace funcionará una vez que el archivo PDF esté en la misma carpeta).---

## 🔗 Relación entre los Ficheros de la Fase

Para que te hagas una idea clara de cómo se complementan los materiales de esta fase, aquí tienes un esquema simplificado de su interconexión:

```mermaid
graph TD
    A[README.md] --> B(Intro_ML.ipynb);
    A --> C(Titanic_Dataset.ipynb);
    A --> D(Guía_Conceptos_ML.pdf);
    A --> E(Recursos_Python_Jupyter.md);
    B --> F(Ejemplos Cotidianos de ML);
    B --> G(Definición y Tipos de ML);
    B --> H(Tu Primer Contacto con Python - Clasificación Sencilla);
    C --> I(Carga y Exploración Inicial);
    C --> J(Variables Objetivo y Características);
    D --> K(Teoría Esencial de ML);
    D --> L(Algoritmos Supervisados/No Supervisados - Intuitivo);
    E --> M(Comandos Básicos de Python);
    E --> N(Uso de Jupyter/Colab);
    B --- D;
    C --- D;
    B --- E;
    C --- E;
