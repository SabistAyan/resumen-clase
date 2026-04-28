# Resumen de Clase: Ramas y Gitflow basico (Branches & Merge)

**Estudiante:** Sebastian Ruben Chavez Sempertegui
**Fecha:** 28 de abril de 2026

## **Gestión de Ramas (git branch)**

Las ramas son líneas de tiempo paralelas que nos permiten experimentar sin alterar la versión estable del proyecto (master). Es como crear una copia de seguridad viva para trabajar en una nueva funcionalidad.

### _git branch <nombre>:_

Crea una nueva rama a partir del punto actual.

### _git branch:_

Lista todas las ramas locales. La que tiene el asterisco (\*) es en la que estás parado actualmente.

### _git branch -d <nombre>:_

Elimina una rama. Git solo te dejará hacerlo si ya fusionaste los cambios para no perder información.

## **Navegación entre Ramas (Checkout)**

Para movernos de una línea de tiempo a otra, utilizamos el comando de salto. Esto actualiza los archivos en nuestra carpeta de trabajo para que coincidan con la versión de la rama elegida.

### _Saltar a una rama:_

git checkout <nombre-de-la-rama>

### _Crear y saltar (Acceso directo):_

git checkout -b <nombre-de-la-rama> (Crea la rama y te posiciona en ella en un solo paso).

## **Git Checkout vs. Git Switch**

Aunque ambos comandos se usan para cambiar de rama, Git introdujo switch en versiones recientes para separar las responsabilidades, ya que checkout hacía demasiadas cosas a la vez.

### _git checkout <rama>:_

El comando clásico. Sirve para cambiar de rama, pero también para restaurar archivos o viajar a commits antiguos (Detached HEAD).

### _git switch <rama>:_

Un comando más específico y seguro. Su única función es cambiar entre ramas.

### _git switch -c <nombre>:_

Equivale al antiguo checkout -b para crear y saltar a una rama nueva.

## **GitFlow Básico: ¿Qué es?**

GitFlow es un modelo de diseño de ramas (workflow) creado por Vincent Driessen. No es una función nueva de Git, sino una metodología o "reglas del juego" para organizar cómo y cuándo se crean ramas en proyectos grandes o profesionales.

## **¿Cómo funciona GitFlow?**

Se basa en mantener dos ramas principales con vida infinita:

### _Master / Main:_

Contiene el código oficial que ya funciona y está en producción.

### _Develop:_

Es la rama de integración. Aquí es donde se junta todo el código nuevo que se está probando antes de pasarlo a Master.

## **Ramas de Apoyo (Supporting Branches)**

Para mantener el orden, GitFlow utiliza tres tipos de ramas temporales que se borran una vez cumplen su objetivo:

### _Feature branches:_

Se usan para desarrollar nuevas funcionalidades. Nacen de develop y vuelven a develop.

### _Release branches:_

Se crean cuando el proyecto ya tiene lo necesario para una nueva versión. Sirven para pulir errores finales antes de lanzar a master.

### _Hotfix branches:_

Son ramas de emergencia. Si hay un error crítico en master que debe arreglarse ya mismo, se crea un hotfix, se repara y se fusiona tanto en master como en develop.
