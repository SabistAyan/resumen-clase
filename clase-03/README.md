# **Resumen de Clase: GitHub y SSH**

### **Estudiante:** Sebastian Ruben Chavez Sempertegui

### **Fecha:** 23 de abril de 2026

## **GitHub vs. Git**

Es importante entender que no son lo mismo:

### _Git:_

Es el sistema de control de versiones que crea los "puntos de guardado" localmente.

### _GitHub:_

Es una plataforma en la nube y red social para desarrolladores que permite alojar, gestionar y colaborar en proyectos usando Git.

## **SSH vs. HTTPS**

Existen dos formas principales de conectar tu PC con GitHub:

### _HTTPS:_

Es cansino y molesto porque pide autenticación (usuario o token) casi cada vez que quieres subir algo.

### _SSH (Recomendado):_

Configuras una llave (key) en tu computadora que GitHub reconoce automáticamente, eliminando la necesidad de loguearte constantemente.

## **Configuración de la Llave SSH**

Para establecer esta conexión segura, se siguen estos pasos en la terminal:

### _Generar la llave:_

ssh-keygen -t ed25519 -C "tu-correo@email.com"

### _Ver y copiar la llave:_

cat ~/.ssh/id_ed25519.pub

### _Vincular con GitHub:_

Copiar el contenido y pegarlo en la sección "SSH and GPG keys" de tu perfil de GitHub.

Probar conexión: ssh -T git@github.com

## **Gestión del Repositorio Remoto**

Vincular un repositorio existente:
Si ya tienes tu repo local iniciado, usa estos comandos para conectarlo a la nube:

git remote add origin git@github.com:TuUser/TuRepo.git

git branch -M main (o master)

git push -u origin main

"Origin" es simplemente el apodo que Git le da por defecto a la URL de tu servidor remoto.

### _Clonar y Modificar:_

### _Clonar:_

git clone "url-del-repo" (Crea una copia local de un proyecto que ya está en la nube).

### _Subir cambios:_

git push origin <rama>

### _Bajar cambios:_

git pull origin <rama>
