# Resumen de Clase: Estados de Git y Commits

**Estudiante:** Sebastian Ruben Chavez Sempertegui
**Fecha:** 22 de abril de 2026

## 1. Los Estados de Git

En Git, los archivos pasan por un ciclo de vida que se divide en tres áreas principales:

1. **Directorio de Trabajo (Modificado):** Es tu carpeta local donde creas o editas archivos. Aquí los cambios están "untracked" (si son nuevos) o "modified" (si ya existían), pero aún no están asegurados por Git.
2. **Stage Area (Preparado):** Es el área de espera o "carrito de compras". Aquí seleccionas qué cambios específicos quieres incluir en tu próximo guardado.
3. **Repositorio Local (Confirmado):** Es el historial oficial. Una vez aquí, los cambios ya tienen un ID único (hash) y son parte de la historia del proyecto.


## 2. Comandos de Gestión de Estados

Para mover archivos entre estos estados, utilizamos los siguientes comandos:

- **Preparar archivos:** `git add <archivo>` (uno por uno) o `git add .` (todos los cambios).
- **Ver el estado actual:** `git status` (nos indica qué archivos están en rojo o verde).
- **Sacar del Stage Area:** `git restore --staged <archivo>` (vuelve al estado modificado sin borrar tus cambios).
- **Descartar cambios físicos:** `git restore <archivo>` (revierte el archivo a su estado original; ¡úsalo con cuidado ya que borra lo que escribiste!).


## 3. El Commit (Punto de Guardado)

El commit es la acción de grabar tus progresos en el historial. Es como un "checkpoint" en un videojuego.

- **Comando básico:** `git commit -m "mensaje"`.
- **Deshacer el último commit:** `git reset --soft HEAD~1` (mantiene tus archivos en el Stage Area para que puedas corregirlos).


## 4. Buenas Prácticas para Commits

Los **commits atómicos** son una práctica donde cada confirmación representa un único cambio lógico, pequeño y completo en el código fuente.

- **Frecuencia:** Es mejor hacer commits pequeños a menudo, agrupando mejoras o acciones específicas, que un commit gigante con todo lo que se quiere hacer.
- **Significado:** Hacer commits a menudo no significa hacerlos sin sentido; deben grabar progresos en iteraciones pequeñas que tengan significado.
- **Integridad:** En lo posible, tus commits no deben dejar la aplicación o el proyecto sin funcionar.


## 5. Cómo escribir Buenos Mensajes de Commit

Un mensaje debe describir lo que hace el commit en pocas palabras y de manera efectiva siguiendo estas reglas:

1. **Usa verbos imperativos:**
   - **Add:** Se añade un nuevo archivo.
   - **Change:** Se modifica un archivo existente.
   - **Fix:** Se arregla un bug.
   - **Remove:** Se elimina un archivo existente.
2. **Sin puntuación innecesaria:** No uses punto final ni puntos suspensivos al final de tus mensajes. Cada carácter cuenta y no debe desperdiciarse en puntos innecesarios.
   - _Mal:_ `git commit -m "Add new search feature."`
   - _Bien:_ `git commit -m "Change the default system color"`

3. **Límite de 50 caracteres:** Sé corto y conciso. Si tienes mucho que explicar, es probable que tu commit contenga demasiados cambios y deba separarse en varios commits.


## 6. Commits Semánticos (Prefijos)

Para que el historial sea legible, se utiliza el formato `prefijo: descripción`[cite: 91]. Algunos prefijos comunes son:

- **feat:** Nueva característica para el usuario.
- **fix:** Bug que afecta al usuario.
- **perf:** Cambios que mejoran el rendimiento.
- **build:** Cambios en el sistema de build o instalación.
- **ci:** Cambios en la integración continua.
- **docs:** Cambios en la documentación.
- **refactor:** Refactorización como cambios de nombre de variables.
- **style:** Formato, espacios o puntos y coma; no afectan al usuario.
- **test:** Para tests nuevos o existentes.


## 7. Añadir contexto (Cuerpo del Commit)

A veces necesitas proveer más contexto sin saturar el sumario del commit.

- Para esto, utiliza solo el comando `git commit`.
- La **primera línea** será el título (sumario).
- Desde la **segunda línea** en adelante será el cuerpo, donde sí se deben aplicar reglas de puntuación para describir el commit.
