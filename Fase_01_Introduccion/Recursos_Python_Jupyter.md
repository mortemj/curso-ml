# 🐍 Recursos Rápidos: Python y Jupyter/Colab

---

¡Bienvenido a tu guía rápida para empezar con Python y los entornos interactivos de Jupyter Notebooks y Google Colab! Estas herramientas serán tus mejores aliadas en este curso de Machine Learning.

## 🎯 ¿Por Qué Python y Jupyter/Colab?

* **Python:** Es un lenguaje de programación muy popular en ciencia de datos por su **simplicidad y legibilidad**. Cuenta con una comunidad enorme y librerías poderosas (como Pandas y Scikit-learn) que facilitan el trabajo con datos y modelos de ML.
* **Jupyter Notebooks / Google Colab:** Son entornos interactivos que te permiten escribir código Python, ejecutarlo celda por celda, ver los resultados al instante y combinarlo con texto explicativo (como este). Son ideales para la experimentación y para presentar proyectos de forma clara.
    * **Jupyter Notebooks:** Se instalan y ejecutan en tu propio ordenador.
    * **Google Colab:** Es una versión de Jupyter que se ejecuta en la nube de Google. Solo necesitas una cuenta de Google y conexión a internet, ¡sin instalaciones! Es la opción más recomendada si estás empezando y no quieres complicarte con configuraciones locales.

---

## 👩‍💻 Primeros Pasos en Google Colab (Recomendado para Empezar)

1.  **Accede a Google Colab:**
    * Abre tu navegador y ve a [Google Colab](https://colab.research.google.com/).
    * Inicia sesión con tu cuenta de Google.
2.  **Crea un Nuevo Notebook:**
    * Haz clic en `Archivo` > `Nuevo Notebook`.
    * ¡Listo! Ya tienes un entorno de trabajo.
3.  **Renombra tu Notebook:**
    * Haz clic en el nombre del archivo en la parte superior (ej. `Untitled0.ipynb`) y renómbralo a algo significativo (ej. `MiPrimerNotebook.ipynb`).
4.  **Guardar:**
    * Colab guarda tus cambios automáticamente en Google Drive. También puedes ir a `Archivo` > `Guardar una copia en Drive`.
5.  **Abrir un Notebook Existente:**
    * Desde la página de inicio de Colab, puedes `Archivo` > `Abrir Notebook` y seleccionar desde Google Drive o GitHub.

---

## ✍️ Jupyter/Colab: Celdas de Código y Texto

Un notebook se compone de **celdas**. Hay dos tipos principales:

1.  **Celdas de Código:**
    * Aquí escribes tu código Python.
    * Para ejecutar una celda, haz clic en el botón de **"Play" (▶️)** a la izquierda de la celda o presiona `Shift + Enter`.
    * El resultado del código aparecerá justo debajo de la celda.

2.  **Celdas de Texto (Markdown):**
    * Aquí escribes texto, explicaciones, títulos, listas. Se usa un lenguaje sencillo llamado **Markdown**.
    * Para editar una celda de texto, haz doble clic sobre ella.
    * Para ver el formato final, ejecuta la celda (`Shift + Enter`).
    * **Ejemplo de Markdown básico:**
        ```markdown
        # Título Grande
        ## Subtítulo
        - Elemento de lista 1
        - Elemento de lista 2
        **Texto en negrita**
        *Texto en cursiva*
        ```

---

## 🐍 Comandos Básicos de Python para Empezar

Aquí tienes algunos comandos fundamentales que te serán muy útiles:

* **Comentarios:** Usa `#` para añadir notas en tu código. Python ignorará lo que siga al `#` en esa línea.
    ```python
    # Esto es un comentario
    print("Hola Mundo") # Esto también es un comentario
    ```

* **Imprimir Texto o Valores (`print()`):** Para mostrar algo en la pantalla.
    ```python
    print("¡Bienvenido al Machine Learning!")
    nombre = "Estudiante"
    print("Hola,", nombre)
    ```

* **Variables:** Guarda información en un nombre.
    ```python
    edad = 30
    temperatura = 25.5
    es_cierto = True # Valores Booleanos (Verdadero/Falso)
    ```

* **Tipos de Datos Básicos:**
    * `int` (enteros): `10`, `500`
    * `float` (decimales): `3.14`, `0.5`
    * `str` (cadenas de texto): `"Hola"`, `"Machine Learning"`
    * `bool` (booleanos): `True`, `False`

* **Operaciones Matemáticas Básicas:**
    ```python
    suma = 5 + 3     # 8
    resta = 10 - 4   # 6
    multiplicacion = 6 * 7 # 42
    division = 10 / 2 # 5.0
    potencia = 2**3  # 8 (2 elevado a la 3)
    ```

* **Listas (Arrays Básicos):** Colecciones ordenadas de elementos.
    ```python
    numeros = [1, 2, 3, 4, 5]
    nombres = ["Ana", "Juan", "Maria"]
    print(numeros[0]) # Accede al primer elemento (recuerda: en Python se empieza a contar desde 0)
    ```

* **Importar Librerías:** Así es como se añaden funcionalidades extra.
    ```python
    import pandas as pd # Importa la librería Pandas, y le damos un alias 'pd'
    import numpy as np  # Importa NumPy, para operaciones numéricas avanzadas
    ```

---

## 💡 Consejos Rápidos para Aprender

* **¡No tengas miedo de experimentar!** Cambia el código, prueba cosas nuevas. No puedes "romper" nada.
* **Lee los errores:** Al principio pueden parecer intimidantes, pero los mensajes de error te dan pistas sobre qué salió mal.
* **Usa Google:** Si tienes una duda o un error, búscalo. Es la forma en que todos aprendemos.
* **Practica regularmente:** La consistencia es clave para construir memoria muscular en programación.

---

## 🔗 Recursos Adicionales Útiles

* **Documentación oficial de Python:** [docs.python.org/es/3/](https://docs.python.org/es/3/) (para consultas específicas de Python)
* **Documentación de Pandas:** [pandas.pydata.org/docs/](https://pandas.pydata.org/docs/) (para aprender más sobre manejo de datos)
* **Tutoriales de Jupyter:** Busca "Jupyter Notebook tutorial" en YouTube para ver demostraciones visuales.

¡A programar!
