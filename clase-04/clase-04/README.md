**Resumen de Clase: Gestión Remota y Viajes en el Tiempo (Checkout)**
**Estudiante:** Sebastian Ruben Chavez Sempertegui
**Fecha:** 24 de abril de 2026

1. **Gestión Avanzada de Remotos (git remote)**
   El comando _git remote_ es el que le dice a tu Git local a dónde enviar o de dónde traer la información.

_git remote -v:_ Muestra las URLs exactas (de lectura y escritura) a las que apunta tu repositorio. Es vital para verificar si estás usando SSH o HTTPS.

git remote add <apodo> <url>: Vincula tu carpeta local con un repositorio en la nube.

git remote set-url <apodo> <url>: Cambia la dirección de un remoto ya existente (útil si te equivocaste de link o quieres pasar de HTTPS a SSH).

2. **Multiples Llaves SSH**
   Si necesitas manejar varias cuentas de GitHub (por ejemplo, una personal y otra de la facultad), puedes tener "varias llaves para distintas puertas".

Se generan con nombres distintos usando el parámetro -f ~/.ssh/id_nombre.

Se gestionan mediante un archivo llamado config en la carpeta .ssh para que las llaves no choquen entre sí.

3. **Viajando en el tiempo: git checkout**
   Este es uno de los comandos más potentes de Git. Nos permite movernos entre diferentes estados del proyecto.

_¿Para qué sirve?_
_Recuperar:_ Volver a ver archivos que borramos o cambiamos por error.

_Experimentar:_ Probar cambios nuevos sin arruinar la rama principal (master).

_Cambiar de rama:_ Saltarnos de una rama a otra (ej. de master a desarrollo).

El estado "Detached HEAD" (HEAD Desacoplado)
Normalmente, el "puntero" (HEAD) apunta a una rama. Cuando haces checkout a un Hash (un código de commit antiguo), entras en estado desacoplado.

_Eres un espectador:_ Puedes ver el pasado, pero no tienes "cuerpo" (rama).

_Riesgo:_ Si haces cambios y te vas al presente sin crear una rama, esos cambios se perderán en el vacío.

4. **Comandos para viajar**
   Ir al pasado: git checkout <hash_antiguo> (buscas el hash con git log).

_Volver al presente:_ git checkout master (vuelves a la última versión de tu rama principal).

_Viajar y crear una rama:_ git checkout -b <nombre_rama_nueva>. Esto "encarna" tu posición actual en una rama nueva para que tus experimentos no se pierdan.

_Buena Práctica:_ Antes de viajar al pasado, asegúrate de haber hecho commit de lo que estás haciendo en el presente, o Git no te dejará moverte para no perder información.
