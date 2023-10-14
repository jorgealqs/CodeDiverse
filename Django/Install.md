# Instalación de Django en un Servidor Limpio

En este tutorial, te guiaré paso a paso a través del proceso de instalación de Django en un servidor limpio. Django es un marco de trabajo web de Python muy popular que facilita el desarrollo de aplicaciones web potentes y eficientes.

## Requisitos Previos

Antes de comenzar, asegúrate de que tu servidor cumpla con los siguientes requisitos:

- Un sistema operativo Linux (por ejemplo, Ubuntu, CentOS).
- Acceso SSH a tu servidor.
- Python 3.x instalado en tu servidor.

## Pasos

### Paso 1: Actualizar el Sistema

Antes de instalar Django, es una buena práctica actualizar los paquetes del sistema. Ejecuta los siguientes comandos:

```bash
sudo apt update
sudo apt upgrade
```

### Paso 2: Instalar pip

Pip es el sistema de gestión de paquetes de Python y es necesario para instalar Django. Si no lo tienes instalado, puedes hacerlo con:

```bash
sudo apt install python3-pip
```

### Paso 3: Instalar virtualenv

Instala virtualenv, que te permitirá crear entornos virtuales:

```bash
pip3 install virtualenv
```

### Paso 4: Crear un Entorno Virtual

Crea un nuevo directorio para tu proyecto y luego crea un entorno virtual en ese directorio. Por ejemplo:

```bash
mkdir mi_proyecto
cd mi_proyecto
virtualenv venv
```

### Paso 5: Activar el Entorno Virtual

Activa el entorno virtual con el siguiente comando:

```bash
source venv/bin/activate
```

### Paso 6: Instalar Django

Dentro del entorno virtual, instala Django utilizando pip:

```bash
pip install Django
```

### Paso 7: Verificar la Instalación

Para verificar que Django se ha instalado correctamente, ejecuta el siguiente comando:

```bash
python -m django --version
```

Deberías ver la versión de Django instalada.

### Paso 8: Crear un Proyecto Django
Ahora estás listo para crear tu primer proyecto Django. Utiliza el siguiente comando para crear un nuevo proyecto:

```bash
django-admin startproject mi_proyecto
```

Esto creará un directorio llamado "mi_proyecto" con la estructura básica de un proyecto Django.

### Paso 9: Ejecutar el Servidor de Desarrollo

Para probar tu proyecto, ejecuta el servidor de desarrollo de Django con el siguiente comando:

```bash
cd mi_proyecto
python manage.py runserver
```

El servidor estará disponible en http://localhost:8000/.