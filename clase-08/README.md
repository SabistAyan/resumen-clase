# Resumen clase: Guía de Contribución al Open Source (Flujo de André)

**nombre:**Sebastian Ruben Chavez Sempertegui
**fecha:**1 de mayo 2026

Este es el proceso estándar para colaborar en proyectos donde no eres un colaborador invitado directamente.

## El Fork (Copia en la Nube)

**Acción:** Vas al repositorio original en la web de GitHub y presionas el botón Fork.

**Resultado:** Se crea una copia idéntica del proyecto en tu propia cuenta de GitHub.

## Clonar y Configurar

**Comando:** Descargas tu fork a tu computadora.

```Bash
git clone https://github.com/tu-usuario/nombre-del-repo.git
cd nombre-del-repo
```

## Trabajar en una Rama Nueva (Branch)

**Regla de Oro:** Nunca trabajes directamente en main.

**Comando:** Creas una rama específica para tu cambio.

```Bash
git checkout -b docs/mi-mejora-ejemplo
```

## Realizar el Cambio (Commit)

**Acción:** Haces tus mejoras en VS Code y guardas el archivo.

**Comandos:** Preparas y confirmas tus cambios con un mensaje claro.

```Bash
git add .
git commit -m "docs: agrega nota de ejemplo en el README"
```

## Subir a GitHub (Push)

**Comando:** Envías tu nueva rama a tu repositorio remoto.

```Bash
git push -u origin docs/mi-mejora-ejemplo
```

## El Pull Request (PR)

**Acción:** En la terminal aparecerá un enlace; haz clic en él o ve a GitHub.

**Finalización:** Presionas el botón "Create pull request" para que los dueños del proyecto original revisen y acepten tu código.
