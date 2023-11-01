# Crear un Superusuario en PostgreSQL (Dentro de un Contenedor Docker)

A continuación, se describen los pasos para crear un superusuario en PostgreSQL que se está ejecutando dentro de un contenedor Docker. Un superusuario tiene privilegios elevados para realizar tareas administrativas en la base de datos.

## Paso 1: Iniciar el Contenedor PostgreSQL

Asegúrate de que el contenedor de PostgreSQL esté en ejecución. Si no lo está, puedes iniciar el contenedor con el siguiente comando:

```bash
docker start nombre_del_contenedor
```

## Paso 2: Conectarse al Contenedor PostgreSQL

Utiliza el siguiente comando para conectarte al shell de PostgreSQL en el contenedor:

```bash
docker exec -it nombre_del_contenedor psql -U postgres
```

Esto te llevará al shell de PostgreSQL, donde podrás ejecutar comandos SQL.

## Paso 3: Crear un Nuevo Superusuario

Dentro del shell de PostgreSQL, ejecuta el siguiente comando SQL para crear un nuevo superusuario. Reemplaza nuevo_usuario y tu_contraseña con los valores deseados:

```bash
CREATE USER nuevo_usuario WITH SUPERUSER PASSWORD 'tu_contraseña';
```

Esto creará un nuevo usuario con privilegios de superusuario.

## Paso 4: Verificar el Nuevo Usuario

Puedes verificar que el nuevo usuario se haya creado correctamente ejecutando una consulta para listar los usuarios:

```bash
SELECT usename FROM pg_user;
```

Deberías ver el nombre del usuario que acabas de crear en la lista.

## Paso 5: Salir del Shell de PostgreSQL

Para salir del shell de PostgreSQL en el contenedor, puedes usar el comando \q o simplemente presionar Ctrl + D.


# Cambiar de Usuario en PostgreSQL

A continuación, se describen los pasos para cambiar de usuario en una base de datos PostgreSQL mientras estás conectado. Esto es útil cuando necesitas cambiar a un usuario con privilegios diferentes en la misma base de datos.

## Paso 1: Conéctate a la Base de Datos

Asegúrate de estar conectado a la base de datos a la que deseas cambiar de usuario utilizando el usuario actual con el que estás conectado (por ejemplo, el usuario `postgres`).

## Paso 2: Cambiar de Usuario

Utiliza el siguiente comando SQL para cambiar de usuario en PostgreSQL:

```sql
SET ROLE nombre_del_usuario;
```

Reemplaza nombre_del_usuario con el nombre del usuario al que deseas cambiar. Por ejemplo, si deseas cambiar al usuario mi_superadmin, ejecuta:

```sql
SET ROLE mi_superadmin;
```

Ahora estás conectado a la base de datos con el nuevo usuario.


## Paso 3: Verificar el Cambio de Usuario

Puedes verificar que hayas cambiado de usuario correctamente ejecutando la siguiente consulta SQL:

```sql
SELECT current_user;
```

Esto debería mostrar el nombre del usuario al que has cambiado.