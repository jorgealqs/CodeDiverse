# Generar Gráficos de Modelos de Django

Para generar gráficos de modelos de Django, debes seguir los siguientes pasos:

1. **Instalar Graphviz:**

   - En Linux:
     ```
     sudo apt-get install graphviz
     ```

   - En macOS (usando Homebrew):
     ```
     brew install graphviz
     ```

   - En Windows u otras plataformas, descarga Graphviz desde [el sitio oficial](https://graphviz.org/download/).

2. **Instalar bibliotecas Python:**

   Asegúrate de tener las siguientes bibliotecas Python instaladas:
    ```
    pip install pyparsing pydot
    ```


3. **Configurar Opciones Predeterminadas:**

En tu archivo de configuración de Django, puedes definir opciones predeterminadas utilizando la variable `GRAPH_MODELS`:

```python
GRAPH_MODELS = {
  'all_applications': True,
  'group_models': True,
  'app_labels': ["myapp1", "myapp2", "auth"],
}
```


4. **Generar Gráficos:**

Puedes usar el comando graph_models proporcionado por django-extensions para generar los gráficos de modelos. Aquí tienes algunos ejemplos:


Crear un archivo .dot:

```bash
./manage.py graph_models -a > my_project.dot
```

Crear una imagen PNG con agrupación de aplicaciones:

```bash
./manage.py graph_models -a -g -o my_project_visualized.png
```