# Práctica 02: Introducción a Django

## Instrucciones para Clonar y Ejecutar el Proyecto

### 1. Prerrequisitos
Tener instalado:
* **Python 3.10+**
* **Git**

### 2. Clonar el Repositorio
Abre tu terminal y clona este repositorio en tu equipo:
```bash
git clone <URL_DE_TU_REPOSITO_CLONADO>
cd practica02
```

### 3. Crear y Activar el Entorno Virtual
Crea un entorno virtual aislado para manejar las dependencias del proyecto.

* **En Linux / macOS:**
  ```bash
  python3 -m venv .venv
  source .venv/bin/activate
  ```


*(Cuando el prompt de la terminal muestra `(.venv)` al inicio, indica que el entorno está activo).*

### 4. Instalar Dependencias
Instalar los paquetes necesarios registrados en el archivo `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 5. Iniciar el Servidor de Desarrollo
Ejecuta el servidor local de Django:
```bash
python manage.py runserver
```

### 6. Visualizar en el Navegador
Abre tu navegador web e ingresa a la siguiente URL:
```text
http://127.0.0.1:8000/
```

## Preguntas de teoría

### 1. ¿Cuál es la diferencia entre un Proyecto (*project*) y una aplicación (*app*) en la filosofía de Django?
* **Proyecto (*project*):** Representa la configuración global y la infraestructura completa de un sitio o sistema web. Contiene las configuraciones generales (`settings.py`), las rutas principales (`urls.py`), la base de datos y la integración de todos los módulos. Un proyecto está compuesto por una o varias aplicaciones.
* **Aplicación (*app*):** Es un módulo independiente y reutilizable diseñado para realizar una tarea o funcionalidad específica (por ejemplo, un sistema de blog, una pasarela de pagos o un perfil de usuario). Una aplicación puede ser reutilizada en diferentes proyectos de Django.

---

### 2. ¿Por qué es una mala práctica subir la carpeta `venv` al repositorio Git y qué problema solucionamos con `requirements.txt`?
 La carpeta del entorno virtual contiene miles de archivos binarios e instalaciones compiladas específicamente para el sistema operativo y la arquitectura de la computadora del desarrollador. Subirla genera repositorios innecesariamente pesados (cientos de megabytes), provoca conflictos cuando otros desarrolladores usan sistemas operativos distintos y contamina el control de versiones con archivos autogenerados.
 El archivo `requirements.txt` resuelve esto de forma ligera al almacenar únicamente los nombres y las versiones exactas de las librerías necesarias (como `Django==5.0.0`). Ocupa solo unos pocos bytes y permite a cualquier persona instalar exactamente las mismas dependencias de forma limpia y automática en su propio entorno virtual mediante el comando `pip install -r requirements.txt`.