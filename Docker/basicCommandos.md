## Descargar una imagen desde Docker Hub:

- `docker pull`: Para descargar una imagen desde Docker Hub, por ejemplo:

```shell
docker pull ubuntu
```

## Listar imágenes locales:

- `docker images`: Para ver las imágenes descargadas en tu sistema:

```shell
docker images
```

## Ejecutar un contenedor a partir de una imagen:
- `docker run`: Para ejecutar un contenedor a partir de una imagen, por ejemplo:

```shell
docker run ubuntu

docker run -d -p 8081:80 --name otro-contenedor-nginx -v /ruta/del propyecto:/usr/share/nginx/html nginx
```

## Listar contenedores en ejecución:
- `docker ps`: Muestra los contenedores en ejecución:

```shell
docker ps
```

- `docker ps -a`: Muestra todos los contenedores, incluyendo los que no están en ejecución:

```shell
docker ps -a
```

## Detener un contenedor:
- `docker stop <container_id_or_name>`: Para detener un contenedor en ejecución:

```shell
docker stop <container_id_or_name>
```

## Eliminar un contenedor:
- `docker rm <container_id_or_name>`: Para eliminar un contenedor. Asegúrate de que el contenedor esté detenido antes de eliminarlo:

```shell
docker rm <container_id_or_name>
```

## Eliminar una imagen:
- `docker rmi <image_id_or_name>`: Elimina una imagen que ya no necesitas:

```shell
docker rmi <image_id_or_name>
```

## Iniciar un contenedor detenido:
- `docker start <container_id_or_name>`: Inicia un contenedor que está detenido:

```shell
docker start <container_id_or_name>
```