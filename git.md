# GIT NOTES (SISTEMA DE CONTROL DE VERSIONES )

***

## Indice <a id="id-indice"></a>
* [Areas](#id-areas)
* [Comandos Basicos](#id-basic)
    * [config](#id-config)
    * [init](#id-init)
    * [status](#id-status)
    * [add](#id-add)
    * [commit](#id-commit)
    * [log](#id-log)
    * [checkout](#id-checkout)
    * [reset](#id-reset)
    * [restore](#id-restore)
    * [mv](#id-mv)
    * [diff](#id-diff)
    * [remote](#id-remote)
    * [Crear clave SSH](#id-key-ssh)
    * [push](#id-push)
    * [clone](#id-clone)
    * [pull](#id-pull)
    * [branch](#id-branch)
    * [merge](#id-merge)
* [Comandos Avanzados](#id-advance)
    * [rebase](#id-rebase)
    * [stash](#id-stash)
    * [pop](#id-pop)
    * [revert](#id-revert)

***

## Cuenta con 3 areas <a id="id-areas"></a>
- Working Tree 
    : (Directorio de trabajo)
- Staging Area 
    : (Cambios pendiente a ser confirmados)
- Commited
    : (Versiones de programas)

[Indice](#id-indice)

## Comandos basicos <a id="id-basic"></a>

### Configurar <a id="id-config"></a>
    git config --global user.email "correo@correo.com"    #CORREO
    git config --global user.name "tu-nombre"             #USER
    git config --global core.editor "code"                #EDITOR DE TEXTO
    git config --global -e                                #ARCHIVO DE CONFIG.
    git config --global core.autocrlf <valor>             #CARACTERES ESPECIALES (valor = Windows: true || Mac/Linux: input)

    NOTA: En caso de no poner --global solo serviria para el proyecto en cuestion.

[Indice](#id-indice)

### Crear repositorio de git <a id="id-init"></a>
    git init

[Indice](#id-indice)

### Estado actual del repositorio <a id="id-status"></a>
    git status

[Indice](#id-indice)

### Añadir archivo/carpeta al Staging Area <a id="id-add"></a>
    git add <nombre-del-archivo/carpeta>

    NOTA: Esto siempre se hace antes de hacer un nuevo commit

### Añadir todo el contenido de la caprta donde estemos al Staging Area
    git add .

[Indice](#id-indice)

### Realizar commit <a id="id-commit"></a>
    -m: mensaje
    git commit -m "nombre-del-commit"


### Cambiar el titulo del commit anterior
    git commit -amend -m "Titulo-cambiado"

[Indice](#id-indice)

### Ver los commits <a id="id-log"></a>
    git log

### Ver los commits en una sola linea
    git log --oneline

### Ver los commits de forma grafica
    git log --graph

### Ver *m* commits
    git log -n <m>

[Indice](#id-indice)

### Volver a versiones <a id="id-checkout"></a>
    git checkout <iniciales-del-hash-del-commit-que-queremos>
    NOTA: 'HEAD' es como un puntero al ultimo commit

### Volver al ultimo commit hecho
    git checkout master
    NOTA: 'master' es la rama principal, tambien la llaman 'main'

### Crear y cambiar de rama
    -b: branch (rama)
    git checkout -b <nombre-de-la-rama>

### Cambiar de rama
    git checkout <nombre-de-la-rama>

[Indice](#id-indice)

### Deshacer cambios y volver al punto antes del commit con los cambios <a id="id-reset"></a>
    git reset <iniciales-del-hash-del-commit-que-queremos>

### Deshacer cambios y volver al punto antes del commit sin los cambios
    git reset --hard <iniciales-del-hash-del-commit-que-queremos>

[Indice](#id-indice)

### Recuperar archivo borrado <a id="id-restore"></a>
    git restore <nombre-del-archivo>

### Quitar archivo del Staging Area
    git restore --staged <archivo>

[Indice](#id-indice)

### Renombrar archivo <a id="id-mv"></a>
    git mv <nombre-antiguo> <nombre-nuevo>

[Indice](#id-indice)

### Ver cambios <a id="id-diff"></a>
    git diff

### Ver cambios en Staging Area
    git diff --staged

[Indice](#id-indice)

### Añadir repositorio local a la nube <a id="id-remote"></a>
    git remote add origin <codigo-SSH>

[Indice](#id-indice)

### Para subir los cambios a github, necesitamos tener una clave SSH <a id="id-key-ssh"></a>
[Como crear una clave SSH](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Subimos la clave publica a github
    $ cd 
    $ cd .ssh
    $ cat clave-publica.pub
    $ Copiamos y pegamos en github 'SSH and GPG keys'

[Indice](#id-indice)

### Subir repositorio en rama master <a id="id-push"></a>
    git push -u origin master

### Subir repositorio en otra rama
    -u: Crear/acceder a rama en la nube
    git push -u origin <nombre-de-la-rama>

[Indice](#id-indice)

### Descargar repositorio desde correo <a id="id-clone"></a>
    git clone <https>

[Indice](#id-indice)

### Descargar repositorio donde ya se esta iniciado <a id="id-pull"></a>
    git pull 

### Descargar rama 
    git pull origin <nombre-de-la-rama>

[Indice](#id-indice)

### Ver todas la ramas que hay <a id="id-branch"></a>
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

[Indice](#id-indice)

### Para mezclar ramas en remoto, se hace desde el mismo github <a id="id-merge"></a>

### Mezclar ramas de forma local 
###### Para esto tenemos que estar en la rama principal donde queremos mezclar
    git merge <nombre-de-la-rama-que-queremos-mezclar>

[Indice](#id-indice)

## Comandos mas avanzados <a id="id-advance"></a>

### Re-escribir los cambios/commits para posteriormente mezclar ramas <a id="id-rebase"></a>
    -i: interactive
    git rebase -i <nombre-de-la-rama-a-la-que-queremos-mezclar>

[Indice](#id-indice)

### Almacenar cambios aun no commiteados <a id="id-stash"></a>
    git stash

[Indice](#id-indice)

### Recuperar los cambios guardados <a id="id-pop"></a>
    git stash pop

[Indice](#id-indice)

### Revertir cambios <a id="id-revert"></a>
    git revert <hash-commit-para-revertir>

[Indice](#id-indice)