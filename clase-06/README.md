# RESUMEN CLASE: Gestion de Ramas y Sincronizacion en Git

**Estudiante:**Sebastian Ruben Chavez Sempertegui
**Fecha:**29 de abril de 2026

## COMANDOS CRITICOS

### GIT MERGE:

Es la fusión de ramas. Sirve para unir mis commits de una rama a otra para que ambas tengan lo mismo. Uso el flag --no-ff para no perder el historial de la rama aunque la borre después, forzando a que se cree un commit de la fusión.

### GIT FECH:

Es para "ojear" el repositorio remoto. Me permite ver si hubo cambios en la rama o en las ramas hijas sin descargar nada a mis archivos todavía.

### GIT PULL:

Con este traigo los cambios del servidor a mi computadora. Lo ideal es usar git pull origin [rama] para evitar líos al sincronizar.

### GIT PUSH:

Sube mis commits locales a GitHub. Uso git push origin [rama] para estar seguro de a dónde lo mando. Si es la primera vez que subo la rama, uso el flag -u para vincularlas y no tener problemas de permisos.

## FLUJO DE TRABAJO

### Preparación y Actualización

### Me muevo a la rama principal:

git checkout develop.

### Actualizo info:

git fetch y luego bajo los cambios con git pull origin develop.

### Fusiono mi trabajo:

git merge --no-ff [mi-rama].

### Si hay bronca:

Resuelvo los conflictos a mano en los archivos.

### Guardo el arreglo:

git add . y hago el git commit (uso Ctrl + O y Enter para guardar en nano).

### Limpieza y subida:

Borro la rama local que ya no uso con git branch -D [mi-rama] y subo todo con git push origin develop.
