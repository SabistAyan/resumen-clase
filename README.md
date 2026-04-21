# Resumen de Clase: Introducción a Git

**Estudiante:** Sebastian Ruben Chavez Sempertegui  
**Fecha:** 20 de abril de 2026

## 1. ¿Qué es GIT?

Git es una herramienta que sirve para controlar los cambios que haces en tus proyectos, especialmente cuando programas. Básicamente te permite guardar versiones de tu código a lo largo del tiempo, de modo que si en algún momento cometes un error o algo deja de funcionar, puedes volver atrás sin problema. Además, también es muy útil para trabajar en equipo, ya que varias personas pueden hacer cambios en el mismo proyecto sin interferirse entre sí.

## 2. ¿Cómo nació GIT?

Git nació por una necesidad real dentro del desarrollo del kernel de Linux. En 2005, el equipo que trabajaba en el proyecto de Linux kernel usaba una herramienta llamada BitKeeper para gestionar su código, pero hubo problemas con la licencia y dejaron de poder usarla gratuitamente. Entonces, Linus Torvalds decidió crear su propia solución en muy poco tiempo, con la idea de que fuera rápida, eficiente y que permitiera trabajar de forma distribuida (es decir, que cada desarrollador tuviera una copia completa del proyecto). En cuestión de semanas desarrolló Git, enfocándose en el rendimiento, la integridad de los datos y la capacidad de manejar grandes proyectos.

## 3. ¿Cómo instalar GIT?

Para instalar Git, primero tienes que ir a la página oficial de Git y descargar el instalador según tu sistema operativo. Si estás en Windows, descargas el archivo, lo ejecutas y prácticamente vas dando “siguiente” a todo (la configuración por defecto suele estar bien para empezar).

## 4. Configuraciones Básicas

Una vez instalado, es necesario configurar nuestra identidad y el manejo de finales de línea:

- **Nombre de usuario:**
  `git config --global user.name "Sebastian"`
- **Correo electrónico:**
  `git config --global user.email "sebastian.chavez.sempertegui@gmail.com"`
- **Manejo de saltos de línea (Windows):**
  `git config --global core.autocrlf true`

## 5. Archivos esenciales en un repositorio

Todo repositorio profesional debería incluir:

1.  **README.md**: Es el archivo principal de presentación que explica de qué trata el proyecto y cómo utilizarlo.
2.  **.gitignore**: Un archivo de texto que indica a Git qué archivos o carpetas debe ignorar (como archivos temporales, carpetas de configuración del IDE o archivos compilados `.class`).
