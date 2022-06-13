# SISTEMA DE CONTROL DE VERSIONES GIT

***

## Cuenta con 3 areas
- Working Tree 
    : (Directorio de trabajo)
- Staging Area 
    : (Cambios pendiente a ser confirmados)
- Commited
    : (Versiones de programas)

## Comandos basicos

### Configurar 
    git config --global user.email "correo@correo.com"    #CORREO
    git config --global user.name "tu-nombre"             #USER
    git config --global core.editor "code"                #EDITOR DE TEXTO
    git config --global -e                                #ARCHIVO DE CONFIG.
    git config --global core.autocrlf <valor>             #CARACTERES ESPECIALES (valor = Windows: true || Mac/Linux: input)

    NOTA: En caso de no poner --global solo serviria para el proyecto en cuestion.

### Crear repositorio de git
    git init

### Estado actual del repositorio
    git status

### Añadir archivo/carpeta al Staging Area 
    git add <nombre-del-archivo/carpeta>

    NOTA: Esto siempre se hace antes de hacer un nuevo commit

### Añadir todo el contenido de la caprta donde estemos al Staging Area
    git add .

### Realizar commit
    -m: mensaje
    git commit -m "nombre-del-commit"


### Cambiar el titulo del commit anterior
    git commit -amend -m "Titulo-cambiado"

### Ver los commits
    git log

### Ver los commits en una sola linea
    git log --oneline

### Ver los commits de forma grafica
    git log --graph

### Ver *m* commits
    git log -n <m>

### Volver a versiones 
    git checkout <iniciales-del-hash-del-commit-que-queremos>
    NOTA: 'HEAD' es como un puntero al ultimo commit

### Volver al ultimo commit hecho
    git checkout master
    NOTA: 'master' es la rama principal, tambien la llaman 'main'

### Deshacer cambios y volver al punto antes del commit con los cambios
    git reset <iniciales-del-hash-del-commit-que-queremos>

### Deshacer cambios y volver al punto antes del commit sin los cambios
    git reset --hard <iniciales-del-hash-del-commit-que-queremos>

### Recuperar archivo borrado
    git restore <nombre-del-archivo>

### Quitar archivo del Staging Area
    git restore --staged <archivo>

### Renombrar archivo
    git mv <nombre-antiguo> <nombre-nuevo>

### Ver cambios
    git diff

### Ver cambios en Staging Area
    git diff --staged

### Añadir repositorio local a la nube
    git remote add origin <codigo-SSH>

### Para subir los cambios a github, necesitamos tener una clave SSH
[Como crear una clave SSH](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Subimos la clave publica a github
    $ cd 
    $ cd .ssh
    $ cat clave-publica.pub
    $ Copiamos y pegamos en github 'SSH and GPG keys'

### Subir repositorio en rama master
    git push -u origin master

### Subir repositorio en otra rama
    -u: Crear/acceder a rama en la nube
    git push -u origin <nombre-de-la-rama>

### Descargar repositorio desde correo
    git clone <https>

### Descargar repositorio donde ya se esta iniciado
    git pull 

### Descargar rama 
    git pull origin <nombre-de-la-rama>

### Ver todas la ramas que hay
    git branch

### Crear rama
    git branch <nombre-de-la-rama>

### Cambiar nombre de la rama
    -m: move/rename
    -M: move/rename force
    git branch -M <nombre-rama-antigua> <nombre-rama-nueva>

### Borrar rama
    -d: delete
    -D: delete force
    git branch -d <nombre-de-la-rama>

### Crear y cambiar de rama
    -b: branch (rama)
    git checkout -b <nombre-de-la-rama>

### Cambiar de rama
    git checkout <nombre-de-la-rama>

### Para mezclar ramas en remoto, se hace desde el mismo github

### Mezclar ramas de forma local 
###### Para esto tenemos que estar en la rama principal donde queremos mezclar
    git merge <nombre-de-la-rama-que-queremos-mezclar>

## Comandos mas avanzados

### Re-escribir los cambios/commits para posteriormente mezclar ramas
    -i: interactive
    git rebase -i <nombre-de-la-rama-a-la-que-queremos-mezclar>

### Almacenar cambios aun no commiteados
    git stash

### Recuperar los cambios guardados
    git stash pop

### Revertir cambios
    git revert <hash-commit-para-revertir>