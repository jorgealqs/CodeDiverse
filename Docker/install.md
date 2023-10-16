# Guía de Instalación de Docker

Este README te guiará a través del proceso de instalación de Docker en tu sistema. Docker es una plataforma de contenedores que te permite empaquetar, distribuir y ejecutar aplicaciones en entornos aislados.

## Requisitos

- Sistema operativo compatible (Linux, Windows, macOS)
- Conexión a Internet (para la descarga de Docker)
- Permisos de administrador o estar en el grupo `docker` (dependiendo del sistema operativo)

## Pasos de Instalación

Sigue estos pasos para instalar Docker en tu sistema:

### 1. Descarga Docker

Visita el [sitio web oficial de Docker](https://www.docker.com/get-started) y selecciona la versión de Docker que mejor se adapte a tu sistema operativo. Puedes elegir entre Docker Desktop (para Windows y macOS) o Docker Engine (para Linux).

### 2. Instala Docker

- **Linux**:
  1. Abre una terminal.
  2. Ejecuta el siguiente comando para instalar Docker:
     ```
     sudo apt-get update
     sudo apt-get install docker-ce
     ```

- **Windows** y **macOS**:
  1. Descarga el instalador de Docker desde el sitio web oficial.
  2. Ejecuta el instalador y sigue las instrucciones en pantalla.

### 3. Verifica la Instalación

Una vez completada la instalación, verifica que Docker se ha instalado correctamente ejecutando el siguiente comando en una terminal:

```bash
docker --version
```

Deberías ver la versión de Docker instalada.

### 4. Ejecuta un Contenedor de Prueba
Para asegurarte de que Docker está funcionando correctamente, ejecuta un contenedor de prueba, como la imagen de "hello-world". Ejecuta el siguiente comando:

```bash
docker run hello-world
```

Si ves un mensaje indicando que la instalación funciona, ¡Docker está listo para su uso!


# Uso de Docker
Puedes comenzar a usar Docker para crear y ejecutar contenedores. Consulta la  [documentación oficial de Docker](https://docs.docker.com/) para obtener más información sobre cómo usar Docker y administrar contenedores.