# 📦 Guía de Instalación y Uso de Anaconda y Jupyter Notebook (Local)

---

¡Hola! Esta guía es para ti si prefieres trabajar con Python y Jupyter Notebooks **directamente en tu ordenador**, sin depender de una conexión a internet o de Google Colab. Utilizaremos **Anaconda**, una plataforma muy popular que simplifica la instalación y gestión de Python y todas las librerías que necesitarás para Machine Learning.

## 🎯 ¿Por Qué Anaconda?

Anaconda es un **distribuidor de Python y R** que incluye muchas librerías populares (como Pandas, NumPy, Scikit-learn) preinstaladas, así como un entorno de gestión de paquetes (`conda`) y la interfaz de usuario **Anaconda Navigator**, que facilita el lanzamiento de aplicaciones como Jupyter Notebook.

* **Simplifica la instalación:** Evita problemas de compatibilidad y dependencias.
* **Todo incluido:** Viene con la mayoría de las herramientas que necesitarás.
* **Gestión de entornos:** Te permite crear entornos aislados para diferentes proyectos, lo cual es una buena práctica.

---

## ⬇️ Paso 1: Descargar e Instalar Anaconda

1.  **Ve a la página oficial de Anaconda:**
    * Abre tu navegador y visita: [https://www.anaconda.com/download](https://www.anaconda.com/download)

2.  **Descarga el instalador:**
    * Asegúrate de seleccionar la versión adecuada para tu sistema operativo (Windows, macOS, Linux).
    * Elige la versión más reciente de Python (generalmente es la opción por defecto, Python 3.x).
    * Haz clic en el botón de descarga. El archivo será grande (varios cientos de MB), así que puede tardar un poco.

3.  **Ejecuta el instalador:**
    * Una vez descargado, abre el archivo instalador.
    * **Windows:** Haz doble clic en el archivo `.exe`.
    * **macOS:** Haz doble clic en el archivo `.pkg`.
    * **Linux:** Abre una terminal y ejecuta el script `.sh` (ej. `bash ~/Descargas/Anaconda3-2023.09-0-Linux-x86_64.sh`).

4.  **Sigue los pasos de instalación:**
    * Acepta los términos de licencia.
    * Para la mayoría de los usuarios, se recomienda la instalación **"Just Me"** (Solo para mí).
    * **Importante:** Cuando llegues a la pantalla de "Advanced Options" (Opciones Avanzadas), **recomiendo encarecidamente marcar la opción "Add Anaconda to my PATH environment variable" (Añadir Anaconda a mi variable de entorno PATH)**. Esto hará que puedas usar `conda` y `python` directamente desde cualquier terminal. Si no lo haces, tendrás que abrir siempre el "Anaconda Prompt" o "Anaconda Navigator".
    * Haz clic en "Instalar" y espera a que el proceso termine.

5.  **Verifica la instalación (Opcional, pero recomendado):**
    * Abre una **nueva terminal** (o "Anaconda Prompt" en Windows).
    * Escribe `conda --version` y presiona Enter. Debería mostrar la versión de conda.
    * Escribe `python --version` y presiona Enter. Debería mostrar la versión de Python instalada por Anaconda.

---

## 🚀 Paso 2: Iniciar Jupyter Notebook

Hay dos formas principales de iniciar Jupyter Notebook después de instalar Anaconda:

### Opción A: Usando Anaconda Navigator (Recomendado para principiantes)

1.  **Abre Anaconda Navigator:**
    * **Windows:** Busca "Anaconda Navigator" en el menú de inicio y ábrelo.
    * **macOS:** Busca "Anaconda Navigator" en "Aplicaciones" o usando Spotlight.
    * **Linux:** Abre una terminal y escribe `anaconda-navigator`.
2.  **Lanza Jupyter Notebook:**
    * En la interfaz de Anaconda Navigator, verás varias aplicaciones. Busca el recuadro de **"Jupyter Notebook"** y haz clic en el botón **"Launch"** (Lanzar).
3.  Esto abrirá una nueva pestaña en tu navegador web predeterminado, mostrando la interfaz de Jupyter.

### Opción B: Usando la Terminal (Para usuarios más avanzados o si Anaconda Navigator falla)

1.  **Abre una terminal** (o "Anaconda Prompt" en Windows).
2.  **Navega a la carpeta donde quieres guardar tus notebooks:**
    * Usa el comando `cd` (change directory). Por ejemplo, si quieres ir a una carpeta llamada `curso-ml` en tu escritorio:
        `cd Desktop/curso-ml` (macOS/Linux)
        `cd C:\Users\TuUsuario\Desktop\curso-ml` (Windows)
    * **Importante:** Abre Jupyter Notebook desde la carpeta donde tienes tus archivos de curso, para que puedas verlos y abrirlos fácilmente.
3.  **Inicia Jupyter Notebook:**
    * Una vez en la carpeta correcta, simplemente escribe:
        `jupyter notebook`
    * Presiona Enter. Esto iniciará el servidor de Jupyter y abrirá una nueva pestaña en tu navegador web con la interfaz de Jupyter.

---

## 📂 Paso 3: Trabajar con Notebooks en Jupyter Local

La interfaz de Jupyter Notebook en tu navegador es como un explorador de archivos.

1.  **Navegar:** Puedes navegar por tus carpetas hasta encontrar el archivo `.ipynb` que quieres abrir.
2.  **Abrir un Notebook:** Haz clic en el nombre del archivo `.ipynb` para abrirlo en una nueva pestaña.
3.  **Crear un Nuevo Notebook:** En la esquina superior derecha, haz clic en el botón **"New"** (Nuevo) y selecciona "Python 3" (o el kernel de Python que tengas).
4.  **Guardar:** Para guardar los cambios, ve a `File` (Archivo) > `Save and Checkpoint` (Guardar y Puntos de Control). Jupyter también guarda automáticamente de forma regular.
5.  **Cerrar un Notebook:** Es importante "apagar" el kernel cuando terminas para liberar recursos. Ve a `File` > `Close and Halt` (Cerrar y Detener).

---

##  troubleshooting (Resolución de Problemas Comunes)

* **Jupyter no se abre en el navegador:**
    * Asegúrate de que no haya otros programas usando el puerto 8888 (el predeterminado de Jupyter).
    * A veces, simplemente refrescar el navegador o copiar la URL que aparece en la terminal (ej. `http://localhost:8888/?token=...`) y pegarla manualmente en una nueva pestaña del navegador ayuda.
* **"jupyter" no se reconoce como un comando:**
    * Esto significa que Anaconda no se añadió correctamente a tu variable de entorno PATH. Intenta abrir "Anaconda Prompt" (en Windows) y ejecuta `jupyter notebook` desde allí. Si sigue sin funcionar, quizás debas reinstalar Anaconda asegurándote de marcar la opción PATH durante la instalación.
* **Problemas al instalar librerías:**
    * Si necesitas instalar una librería que no viene con Anaconda (ej. `pip install tensorflow`), asegúrate de hacerlo en tu terminal o Anaconda Prompt, no dentro de una celda de Jupyter.

---

¡Ya estás listo para programar en tu entorno local!
