# Proyecto Flask con Docker

Este proyecto contiene una aplicación Flask que se ejecuta dentro de un contenedor Docker. A continuación, se describen los pasos para configurar y ejecutar el proyecto.

## Pasos para ejecutar el proyecto

### 1. Crear el entorno virtual
Aunque no es necesario para Docker, puede crear un entorno virtual para pruebas locales:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 2. Instalar Flask:

```bash
pip install flask
```

### 3. Asegurar la instalación de Docker
Verifique que Docker y Docker Compose estén instalados:

```bash
docker --version
docker-compose --version
```

Si no están instalados, busque en internet cómo instalarlos o utilice herramientas como ChatGPT para obtener ayuda.

### 4. Crear y ejecutar el contenedor Docker

Ejecute el script `sample-app.sh` para construir la imagen Docker y ejecutar el contenedor:

```bash
bash sample-app.sh
```

Este script realiza las siguientes acciones:
- Crea un directorio temporal `tempdir`.
- Copia los archivos necesarios al directorio temporal.
- Genera un `Dockerfile`.
- Construye la imagen Docker con el nombre `sample-app`.
- Ejecuta un contenedor llamado `samplerunning` en el puerto `5050`.

### 5. Verificar la ejecución

Abra un navegador web y acceda a la aplicación en:

```
http://localhost:5050
```

### 6. Detener y limpiar
Para detener y eliminar el contenedor:

```bash
sudo docker stop samplerunning
sudo docker rm samplerunning
```

## Lo que aprendí

### Términos de Docker
- **Imagen Docker**: Una plantilla que contiene todo lo necesario para ejecutar una aplicación.
- **Contenedor Docker**: Una instancia en ejecución de una imagen Docker.
- **Dockerfile**: Un archivo que define cómo construir una imagen Docker.
- **Build**: El proceso de crear una imagen Docker a partir de un Dockerfile.
- **Run**: El comando para iniciar un contenedor Docker.

### Expresiones de Flask
- **Flask**: Un microframework para construir aplicaciones web en Python.
- **Render Template**: Función de Flask para renderizar archivos HTML.
- **Route**: Decorador de Flask para definir rutas URL.

Con estos pasos y conceptos, podrá ejecutar y entender el proyecto sin problemas.