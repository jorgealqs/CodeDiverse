<!-- git clone git@github.com:jorgealqs/CodeDiverse.git
git clone git@github.com:jorgealqs/jorgealqs.github.io.git
pbcopy < ~/.ssh/jorge.pub
eval "$(ssh-agent -s)"
cat jorge.pub
ssh-keygen -t ed25519 -C "joralquisi@hotmail.com"
ssh -V -->
# Cómo Generar y Agregar una Clave SSH a GitHub

## Requisitos Previos
- Asegúrate de tener SSH instalado en tu sistema.

A continuación, se describen los pasos para generar una nueva clave SSH y agregarla a tu cuenta de GitHub en la página web:

1. **Generar una nueva clave SSH**:

    Sustituye "tu-correo-electronico@gmail.com" con tu dirección de correo electrónico. Esto generará una nueva clave SSH.
    ```bash
    ssh-keygen -t ed25519 -C "tu-correo-electronico@gmail.com"
    ```
   

2. **Iniciar el agente SSH:**

    Para que el agente SSH maneje tus claves, ejecuta el siguiente comando:
    ```bash
    eval "$(ssh-agent -s)"
    ```

3. **Copiar la clave SSH al portapapeles:**

    La clave pública que hayas generado es id_ed25519.pub.
    ```bash
    pbcopy < ~/.ssh/id_ed25519.pub
    ```

4. **Agrega tu clave SSH actual a SSH-Agent :**

```bash
ssh-add ~/.ssh/id_ed25519.pub
```

5. **Agregar la clave SSH a tu cuenta de GitHub:**
    - Abre GitHub en tu navegador web.
    - Inicia sesión en tu cuenta de GitHub si aún no lo has hecho.
    - En la esquina superior derecha, haz clic en tu avatar de perfil y selecciona "Settings".
    - En el menú de la izquierda, haz clic en "SSH and GPG keys".
    - Haz clic en el botón "New SSH key" o "Add SSH key".
    - Pega la clave pública en el campo correspondiente y da un nombre descriptivo a la clave.
    - Haz clic en "Add SSH key" para guardar la clave en tu cuenta de GitHub.


