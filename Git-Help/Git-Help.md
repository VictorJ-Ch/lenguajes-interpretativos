# CREAR UN REPOSITORIO POR LÍNEA DE COMANDO EN GIT

## Pasos
 1. git init
 2. git config --local  user.name "Victor Chavarria"
 3. git config --local user.email chavarria.martinez.victor101@gmail.com
 4. git config --local user.ui true
 5. git config --list
    
    1. "q" para quit
 6. git config --global core.editor "code --wait"
 7. git config --local -e
 8. git config --global core.autocrlf true
 9. git config -h (opciones de cofiguración en terminal)
 10. git help config (opcines de la configuración en el navegador)
 11. Creas el repositorio en GitHub (solo le pones el name al repositorio)
 12. en VSC usas los comandos.
 13. git init
 14. git add README.md / git add .
 15. git commit - m "First commit"
 16. gt branch -M main
 17. remote add origin (link que da el repositorio)
 18. git push -u origin main

 ## Para cuando tengas ya el repositorio activo

 1. git init (primera vez que inicializas una carpeta) / git pull
 2. git add .
 3. git commit / git commit -m "lorem"
 4. git push

## Comandos

> **git branch**: Te regresa las remas que tengas en el repositorio.

> **git status**: Muestra el status del repositorio.

> **git checkout (branch)**: Para cambiar entre las ramas.

> **git branch (branch)**: Para crera una rama.

> **gity branch -d (branch)**: Para borrar la rama.

> **git merge (branch)**: Para unir el trabajo de las ramas.

> **git log --online**: Ver status de las ramas.

>**git tag**: Se agrega una etiqueta, paracontrol de versiones en el proyecto. (git tag -> git add . -> git tag "V0.0.0" -> git commit -m "V0.0.0)