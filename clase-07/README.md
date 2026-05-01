# Resumen de clase: Trabajo en Equipo con Git: Uso de Pull Requests paso a paso

**nombre:**Sebastian Ruben Chavez Sempertegui
**fecha:**30 de abril de 2026

## Introducción a los Pull Requests

### ¿Qué es un Pull Request?

Básicamente es la forma profesional de proponer cambios en Git. En lugar de meterle mano al código base directo (como main o develop), levantas la mano y dices: "Oigan, hice esto en mi rama, ¿lo pueden revisar para unirlo al código principal?". Es como pedir permiso y pasar por una auditoría de calidad antes de que tus cambios se vuelvan oficiales.

### Análisis del Tutorial: ¿Cómo crear un PR?

Basado en el flujo del video, así es como lo haría yo paso a paso:

**El Empujón Inicial:**Primero, como siempre, subo mi rama a GitHub con un git push origin mi-rama.

**El "Botón de Pánico":** Apenas entro a mi repositorio en GitHub.com, me va a aparecer un recuadro amarillo que dice "Compare & pull request". Es GitHub avisándome que detectó cambios nuevos.

### Vender mi Cambio:

**Título:**Pongo algo claro, como feat: corrección de estilos en clase-03.

**Descripción:**Aquí explico qué hice. Es clave para que el que revise no esté perdido.

**Revisión Final:** El video muestra que puedes ver el "Diff" (las líneas verdes son lo que añadí y las rojas lo que borré). Le doy a "Create pull request" y listo, el PR queda abierto.

**El Merge Final:**Si todo está bien y no hay conflictos, le doy al botón verde de "Merge pull request". ¡Y pum! Mis cambios ya viven en la rama principal de forma segura.

### ¿Por qué debería importarme esto?

**Orden total:** No rompes la rama principal por error.

**Feedback:**Si trabajas con otros compañeros, ellos pueden comentarte líneas específicas de tu código para mejorarlo antes de fusionar.

**Historial:**Queda un registro de por qué se decidió unir ese código.

**Tip de pro:** Si alguna vez trabajas en un proyecto Open Source o en una empresa, NUNCA vas a hacer push directo a main. Todo, absolutamente todo, pasará por un PR.

## Pull Requests y Seguridad: Blindando el Repositorio

### ¿Por qué complicarse con PRs si ya sé pushear?

La respuesta es simple: Control y Supervivencia. Trabajar sin PRs es como dejar la puerta de tu casa abierta y confiar en que nadie va a entrar a desordenar.

**Filtro de Calidad:** Evitas que alguien suba código que rompa todo el proyecto.

**Debate Técnico:** Obliga al equipo a discutir: "¿Es esta la mejor forma de hacerlo?".

**Seguridad:** Bloqueas posibles ataques o errores críticos antes de que lleguen a la rama principal.

### Análisis del Tutorial: Cómo Proteger las Ramas

El video muestra que aunque sepas hacer PRs, el repositorio sigue "abierto" por defecto. Para cerrarlo de verdad, hay que configurar las Branch Protection Rules en GitHub:

**Ajustes de Rama:** En GitHub, vas a Settings > Branches.

**Añadir Regla:** Le das a "Add branch protection rule" y escribes el nombre de la rama que quieres proteger (normalmente main o develop).

**El Candado Maestro:** Activas la opción "Require a pull request before merging".

**Importante:** También puedes activar "Require approvals" para que, por ley, una o dos personas tengan que darte el visto bueno (el famoso "Approve") antes de que el botón de Merge se ponga verde.

**Bloqueo de Push Directo:** Con esto activado, si alguien intenta hacer un git push origin main desde su terminal, Git le va a rebotar el comando con un error. Ahora el PR es obligatorio.

### Mi Flujo de Trabajo (Con Pull Requests)

Este es mi nuevo estándar para no romper nada:

**Sincronizo:** Me pongo en develop, hago fetch y pull para estar al día.

**Rama Nueva:** Salto a mi rama de trabajo (git checkout -b mi-mejorora).

**Actualización Constante:** Si develop cambia mientras yo trabajo, traigo esos cambios a mi rama con git merge develop para no tener sorpresas al final.

**Subida Segura:** Hago el push de mi rama y, en lugar de fusionar yo mismo, me voy a GitHub a abrir el Pull Request.

**Revisión y Limpieza:** Una vez que mi PR es aprobado y mergeado en la web, borro mi rama local y repito el ciclo.

**Nota para mi "yo" del futuro:** Si el PR tiene conflictos, los resuelvo en mi laptop usando VS Code antes de volver a pushear. ¡Nunca mandes un PR con conflictos sin resolver!.

## Colaboración Externa: El Flujo del "Fork"

Si no eres un colaborador invitado (es decir, no tienes permisos de escritura directos), no puedes hacer push a ese repositorio. Para colaborar, debes seguir el flujo de Fork & Pull Request.

### El "Fork" (Tu propia copia)

Como no puedes tocar el repositorio original, vas a GitHub y le das al botón de Fork.

Esto crea una copia exacta del proyecto en tu cuenta de GitHub.

Ahora tú eres el dueño de esa copia y ahí sí tienes permiso de hacer lo que quieras.

### Clonar y Trabajar

Ahora trabajas en tu copia como si fuera cualquier otro proyecto:

git clone [URL-de-tu-fork].

Creas una rama nueva para tu mejora: git checkout -b mi-aporte.

Haces tus cambios, git add y git commit.

Subes los cambios a tu GitHub: git push origin mi-aporte.

### El Puente: Pull Request entre Repositorios

Aquí es donde sucede la magia que explicó Andre:

Vas a la página de tu fork en GitHub.

GitHub detectará que tu rama tiene cambios que el repositorio original no tiene y te ofrecerá crear un Pull Request.

Al darle click, estarás enviando tus cambios desde tu cuenta hacia la cuenta del dueño original.

### ¿Por qué es mejor este flujo? (Análisis del Video uwu)

Andre nos muestra que este método es el más seguro del mundo porque:

**Cero Riesgo:** El dueño del proyecto original no tiene que darte contraseñas ni permisos.

**Control Total:** El dueño recibe tu propuesta y puede ver exactamente qué líneas cambiaste antes de decidir si las acepta o no.

**Independencia:** Tú puedes seguir mejorando tu fork sin afectar a nadie más hasta que decidas enviar el PR.

**Resumen para mis notas:**
"Si no estoy invitado, no lloro. Hago un Fork, trabajo en mi copia, y luego le mando un Pull Request al dueño original para que vea mi talento. Es la forma más pro de colaborar en proyectos ajenos."
