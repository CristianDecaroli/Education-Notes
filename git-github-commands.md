# Git and GitHub commands

1. **Conectar/clonar un repositorio de GitHub.**

```bash
git clone https://github.com/username/reponame
```

2. **Preparar nuevos archivos y/o modificaciones que se realizaron posterior a la clonación.**

```bash
git add .
```

3. **Commitear los archivos agregados**

```bash
git commit -m 'nombre_del_commit'
```

4. **Por buenas prácticas, intentamos traernos los archivos existentes en el repo remoto.**

```bash
git pull origin main
```

5. **Subimos los archivos pendientes al repo remoto**

```bash
git push origin main
```

En este momento se nos pedirá colocar el nombre de usuario del repositorio de GitHub y también el TOCKEN (password). Este tocken debe crearse desde GitHub Settings/Developer Settings/Personal Access Tocken/Tockens(classic). Este tocken servirá como password en este paso. Debemos guardarlo y tener presente el tiempo de caducidad elegido. Todos los tockens se pueden eliminar. 

Tener presente que la rama (branch) deben coincidir tanto en el repositorio local como el remoto. Para cambiar el nombre de la rama local podemos ejecutar el comando `git branch -m 'nombre_de_la_rama'`

Para listar las ramas (branches) disponibles en tu repositorio local de Git, puedes utilizar el comando `git branch`. Este comando te mostrará una lista de todas las ramas presentes en tu repositorio local y resaltará la rama en la que te encuentras actualmente.

Para listar las ramas remotas y locales lo podemos hacer con el comando `git branch -a`

Para ver los últimos commits de cada rama junto con la lista de ramas `git branch -v`.

