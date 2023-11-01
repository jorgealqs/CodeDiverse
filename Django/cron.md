# Configuración de Tareas Programadas en Django

Para configurar tareas programadas en Django, puedes seguir los siguientes pasos:

1. **Instalar `django-crontab`:**

    Utiliza el siguiente comando para instalar la biblioteca `django-crontab`:

    ```
    pip install django-crontab
    ```

2. **Añadir a `INSTALLED_APPS` en settings.py:**

Agrega `'django_crontab'` a la lista de aplicaciones instaladas en tu archivo `settings.py`:
```python
INSTALLED_APPS = (
    'django_crontab',
    ...
)
```

3. **Crear un método programado:**

Define un nuevo método que debe ejecutarse periódicamente mediante cron en tu archivo cron.py dentro de tu aplicación (por ejemplo, myapp):

```python
def mi_tarea_programada():
    pass
```

4. **Agregar la tarea programada a CRONJOBS en settings.py:**

En tu archivo settings.py, define la tarea programada en la lista CRONJOBS junto con su programación. Por ejemplo:
```python
CRONJOBS = [
    ('*/5 * * * *', 'myapp.cron.mi_tarea_programada')
]
```

5. **Ejecutar el comando para agregar las tareas programadas:**

Ejecuta el siguiente comando para agregar todas las tareas definidas en CRONJOBS al crontab del usuario con el que estás ejecutando este comando:
```jorgealqs
python manage.py crontab add
```

6. **Ver tareas activas:**

Para ver las tareas programadas activas en este proyecto, puedes ejecutar:
```jorgealqs
python manage.py crontab show
```

7. **Eliminar tareas programadas:**

Eliminar todas las tareas programadas definidas es sencillo:

```jorgealqs
python manage.py crontab remove
```

8. **Eliminar una tarea programada específica:**

Para eliminar una tarea programada específica, primero identifica su programación y el nombre del método asociado. Luego, puedes utilizar el siguiente comando para eliminarla:

```jorgealqs
python manage.py crontab remove <programación> <nombre_del_método>

```