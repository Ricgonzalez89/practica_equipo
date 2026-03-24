# Prácticas - Laboratorio I

Este espacio fue creado con el objetivo de realizar prácticas a modo de entender cómo se integra **Git** como *Sistema de Control de Versiones* en la vida diaria de un *Programador* y el uso de **GitHub** como entorno de trabajo.

## Áreas de Git

Las **tres áreas principales** de **Git** son:

#### 1. **Working Directory** (Directorio de Trabajo).
- Es donde tienes tus archivos locales.
- Aquí es donde editas, creas y modificas archivos.
- Los cambios aquí no están rastreados por **Git** hasta que los agregues.

#### 2. **Staging Area** (Área de Preparación / Index)
- Es el área intermedia.
- Aquí preparas los cambios que quieres incluir en el próximo *commit*.
- Los archivos están **"staged"** pero aún no guardados permanentemente.

#### 3. **Repository** (Repositorio / .git directory)
- Es donde **Git** almacena permanentemente los commits.
- Contiene todo el historial del proyecto.
- Los cambios aquí son inmutables (una vez commiteados).

## Comandos Git
Comandos donde se use ej: `<Nombre>`, no se usan los `<>`

- <kbd>$ ls</kbd> - Visualiza los archivos dentro del repositorio.
- <kbd>$ pwd</kbd> - Indica donde estamos posicionados en el directorio.
- <kbd>$ clear</kbd> - Limpia la consola o terminal de comandos.
- <kbd>$ cd ../</kbd> - Regresa a la carpeta anterior.
- <kbd>$ cd <Nombre de la carpeta></kbd> - Moverse entre carpetas del directorio.
- <kbd>$ mkdir <Nombre de la carpeta></kbd> - Crea una carpeta la carpeta.
- <kbd>$ rmdir <Nombre de la carpeta></kbd> - Elimina la carpeta del nombre mencionado.
- <kbd>$ git add <Nombre del archivo></kbd> - Agrega un archivo al *área de preparación*.
- <kbd>$ git status</kbd> - Muestra información sobre el status del *área de preparación*.
- <kbd>$ git commit -a</kbd> - Hace *Commit* de los archivos del repositorio sin pasar por el *área de preparación*.
- <kbd>$ git commit -m "Descripción del Commit"</kbd> - Hace *Commit* de los archivos que se encuentran en el *área de preparación*.
- <kbd>$ git config --list</kbd> - Lista de configuraciones de **Git**.
- <kbd>$ git config --global --list</kbd> - Lista de configuraciones globales de **Git**.
- <kbd>$ git rm --cached <Nombre del archivo></kbd> - Quita un archivo del *área de preparación*.

## Configuración Inicial de Git

```bash
# Establece el Alias
1. $ git config --global user.name "Alias de Usuario"

# Establece el Correo Electrónico
2. $ git config --global user.email "Correo Electrónico del Usuario de GitHub"

# Establece VSCode como Editor de Código para la Configuración Global
3. $ git config --global core.editor "code --wait"

# Configurar Color de la UI (opcional)
4. $ git config --global color.ui true

# Establecer Salto de Línea de forma automática para subir al servidor
5. $ git config --global core.autocrlf true
```

## Inicializar un Nuevo Repositorio

Se coloca la letra del disco donde se quiera crear el repositorio, ej: <kbd>$ cd e:</kbd>

```bash
# Moverse entre Discos
1. $ cd <Letra del disco>:

# Crea una carpeta
2. $ mkdir <Nombre de la carpeta>

# Entrar a la carpeta creada
3. $ cd <Nombre de la carpeta>

# Inicializar Git
4. $ git init
```

## Subir Archivos al Repositorio

```bash
# Agrega un archivo al área de preparación
1. $ git add <Nombre del archivo>

# Comprueba que el archivo fue agregado (opcional)
2. $ git status

# Hacer Commit de los archivos que se encuentran en el área de preparación
3. $ git commit -m "Descripción de los cambios realizados"
```

## Eliminar Archivos del Repositorio

```bash
# Remueve el archivo a eliminar
1. $ rm <Nombre del archivo>

# Comprobar que el archivo fue removido del directorio (opcional)
2. $ git status

# Agrega el archivo removido anteriormente al área de preparación
3. $ git add <Nombre del archivo removido>

# Hacer Commit de los cambios aplicados recientemente en el área de preparación
4. $ git commit -m "Eliminación del archivo"
```

## Ramas del Repositorio

- El nombre de las ramas creadas deben ser en *minúsculas* y en lugar de espacios se usa `-` entre cada palabra.
- Antes de eliminar o cambiar el nombre de una rama, debe asegurar que está posicionado en otra rama distinta a la que se va a eliminar o cambiar el nombre.
- Al momento de fusionar una rama, se debe estar en la rama en la que se quiere hacer la fusión.

```bash
# Muestra las ramas creadas en el repositorio
1. $ git branch

# Crea una Nueva Rama
2. $ git branch <nombre-de-la-rama>

# Se posiciona en la rama donde te encuentras
3. $ git switch <Nombre de la Rama>

# Elimina una rama del repositorio
4. $ git branch -d <nombre-de-la-rama>

# Cambiar el nombre de una rama
5. $ git branch -m <nombre-actual-de-la-rama> <nombre-nuevo-de-la-rama>

# Fusiona una rama con otra
6. $ git merge <Nombre de la Rama>
```

## Git Clone, Push y Pull

```bash
# Clona el repositorio desde GitHub a nuestro repositorio local
1. $ git clone <URL del repositorio a importar desde GitHub>

# Envia los Commits realizados en el repositorio local a GitHub
2. $ git push origin main

# Actualiza automáticamente el repositorio local con los cambios hechos en el repositorio de GitHub
3. $ git pull
```

## Comandos de Utilidad Extra

- Los archivos se pueden recuperar solo si fueron agregados anteriormente al *área de preparación*.
- Volver al último *Commit* de un archivo resetea la información del mismo al último *Commit* hecho.

```bash
# Restaura un archivo desde el área de preparación
$ git restore <Nombre del archivo>

# Volver al último Commit de un archivo
$ git checkout <Nombre del archivo>

# Resetea los cambios agregados en el área de preparación
$ git reset --hard

# Cambia el nombre de un archivo dentro del repositorio
$ git mv <Nombre actual del archivo> <Nombre nuevo del archivo>

# Muestra el status del área de preparación de forma simple
$ git status -s

# Compara la versión de un archivo en el área de preparación con el último Commit
$ git diff --staged

# Muestra información sobre los Commit de una rama de forma simple
$ git log --oneline

# Compara dos Commit usando su ID
$ git diff <ID del Commit 1> <ID del Commit 2>
```

## Más Información

Para profundizar más sobre la edición del **README.md** puedes revisar la documentación oficial sobre el formato [Markdown](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
