# PRACTICAS

- [Practica 1 "Información Personal"](./VictorChavarria-Practices/Practices/practica-1/practica-1.md)
- [Practica 5 "Cuestionario Markdown"](./VictorChavarria-Practices/Practices/practica-5/practica-5.md)

## INFORMACIÓN DE GIT

- [Help](./Git-Help/Git-Help.md)

## Materias

> **Lenguajes interpretativos**: _Prof: Jonathan Miranda_ En esta materia estoy aprendiendo el uso de repositorios, por medio del terminal, mediante Git.

> **Sistemas operativos**: _Prof: Osiel Morales_ En esta materia estoy aprendiendo del uso de la computadora, su mantenimiento y demás procesos para la instalación de varios sistemas operativos, dentro de una misma computadora, igualmente aprendo de la gestión de recursos de la misma.

> **Principios de composición y diseño**: _Prof: Roberto Melo_ En esta materia estoy aprendiendo a usar Photoshop.

> **Diseño de videojuegos**: _Prof: Hector Guerrero_ En esta materia estoy aprendiendo distintops motores gráficos, gestión de proyectos y creación de proyectos.

> **Proyecto de app: _Prof: Sebastián Mejia_ En esta materia estoy aprendiendo a crear documentación, para proyectos con software especializado.

## Cuestionario

1. _**¿Cómo se inicializa un repositorio en Git?**_

    Al momento de configurar por primera vez el Git, en el repositorio que hemos creado en el GItHub.

    Primero que nada configuram,os tu usuario que va a ser quien registre el git, al momentoi de subir los cambios.

    ```bash
    git init
    git config --local user.name "Aquí pones tu nombre"
    git config --git confign --local user.email "Aquí colocas tu correo con el que estas en el GitHub"
    git config --local user-ui true
    git config --list
    ```

    En el anterior hay que considerar que esa configuración es para cuando trabajas en una computadora de la empresa, por eso es que se pone "--local", pero en caso contraqrio donde estes trabajando en un computadora propia, donde solo seas vos quien la use solo se cambia de "--local" a "--global", quedando el código tal que así.

    ```bash
    git init
    git config --global user.name "Aquí pones tu nombre"
    git config --git confign --global user.email "Aquí colocas tu correo con el que estas en el GitHub"
    git config --global user-ui true
    git config --list
    ```

    Ahora asignamos a VSC como editor de configuración de Git.
    ``` bash
    git config --global core.editor "code --wait"
    git config --local -e
    ```
    en caso de que seas soo vos.
     ``` bash
    git config --global core.editor "code --wait"
    git config --global -e
    ```
    Ahora solo estandarizamos las lineas en Windows.
    ``` bash
    git config --global core.autocrlf true
    ``` 
    en caso de que lo trabajes en Linux o Mac la línea cambia un poco y queda tal que así.
    ```bash
    git config --global core.autocrlf input
    ```

2. ¿Cómo creas nun repositorio en GitHub?
    1. Entras a la web de GitHub.
    2. Inicias sesión o te registras.
    3. Debajo de la barra de busqueda, de la web, podemos encontrar el Header de GItHub, de ahi hasta la parte de la derecha, podemos encontrar un ícono con el simbolo de "+" con una flecha abajo "catálogo", le damos click.
    4. Una vrez dado el click se nos abrirá un menú con varias opciones, le damos click en "New repository".
    5. Te dirigirá  la página de creación del repositorio, ahí lo que harás será darle un nombre al repositorio, debajo de la sección que dice "Repository name*".
    6. Si queres les podes dr una descripción de lo va a ser el repositorio.
    7. El resto de cosas las dejas tal y como está

3. ¿Cómo vinculas un repositorio local de git con uno remoto en GitHub?

    Par poder trabajar en la carpeta tenes que ligar el repositorio local con el remoto, para que cuando trabajes en otro laso, podas ver todo lo que haz hecho antes.
    
    Para lo anterior, es necesario tener creado el repositorio en el GitHub y haqber inicializado el repositorio con su configuración en el Git (Terminal).

    En el terminal solo pones.
    ```bash
    git init
    git add README.md
    git commitm -m "First commit"
    git branch -M  main
    remote add origin (Aqui colocas el link que os debió de aparecer al hacer el repowitorio en el GitHub).
    git push -u origin main
    ```

4. ¿Cuál es el flujo básico de trabajo en Git y GitHub?
Al trabajar en un repositorio podemos toparnos con distintas interfaces, las cuales podemos encontrar cierto vocabulario que debemos que saber, al momento de trabajr en repositorios.

> **Working directory**: Al momento de trabajar y hacer cambios, estos solo se van a guardar en el local, y no se verá reflejado en el remoto.

> **Staging area**: en muchas interfaces se le conoce como "astaged" los cambios dentro, significa que pueden ser comprometidos, lo que nos va a llevar a que estos cambios que hicimos en el local se reflejen en el remoto.

> **Local repository**: Es el commit, es donde se va a subir a tu repositorio y que se va poder ver reflejado como en el historial de cambios hechos (se llaman commits por eso).

> **Remote repository**: En este para que todos los cambios que hagamos en el local, si los queremos ver reflejados en el remote, podemos usar el "push", y así podemos verlo reflejados en el remote.

Al momento de trabajar en Git podemos usar esta linea de comandos.

```bash
git init
git pull
git add .
git commit -m "Nombre de commit"
git push
```