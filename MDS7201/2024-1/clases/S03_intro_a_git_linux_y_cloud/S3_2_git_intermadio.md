# Workshop - Git Intermedio

## Punteo

- Repaso de conceptos básicos
	- Para qué y por qué usar git
	- Origen
	- Importancia en el trabajo de un DA o DS
	- Tipos de objetos
		- Blobs
		- Trees
		- Commits
	- Punteros
		- Branches
		- Tags
	- Comandos básicos
		- `git clone`
		- `git init`
		- `git status`
		- `git config`
		- `git add`
		- `git commit`
			- `git commit -am "message"`
		- `git fetch`
		- `git merge`
		- `git pull`
		- `git push`
		- `git branch`
		- `git tag`
		- `git checkout`
		- `git remote`
		- `git rebase`
	- Ambientes de trabajo
		- Working copy
		- Staging area
		- Local repository
		- Remote repository
		- Múltiples remotos
- `~/.gitconfig`
	-  `git config --global user.name "Mona Lisa"`
	- `git config --global user.email "monalisa@louvre.fr"`
- `<git-repo>\.git\config`
	- `git config user.name "Mona Lisa"`
	- `git config user.email "monalisa@louvre.fr"`
- `~/.gitcredentials`
- Configurando múltiples remotos
	- `git remote add origin https://github.com/OWNER/REPOSITORY.git`

-----------------
### Ejercicio 1: 
Cada uno cree su propio repo en una cuenta de GitHub, clónelo, configure su usuario localmente y explorar `~/.gitconfig` y `~/.gitcredentials`. Finalmente, agregar un nuevo remoto por compañero de equipo.

-----------------
- Guía de estilo para commits
	- Explicar el qué y por qué
	- Cómo escribirlo
	- Tipos de commits
- README.md y Markdown
- Aliases
	- Comandos más usados
	- `git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative"`
	- `git config --global alias.co "chechout"`
	- `git config --global alias.st "status"`
	- etc

-----------------
### Ejercicio 2: 
Setear algunos alias y commitear un README.md usando esos alias.

-----------------
- Branching strategies
	- Branching strategy Comunidad de Analytics
	- GitFlow
		- `git flow init`
		- `git flow feature start feature_branch`
		- `git flow feature finish feature_branch`
		- `git flow release start 0.1.0`
		- `git flow release start 0.1.0`
		- `git flow hotfix start hotfix_branch`
		- `git flow hotfix finish hotfix_branch`

-----------------
### Ejercicio 3: 
Simular un desarrollo de proyecto solo creado archivos y comiteándolos por separado, con buenos mensajes de commit y usando git flow.

-----------------
- Cuándo ocurren conflictos
	- `git merge`
	- `git pull`
	- `git rebase`
	- `git stash apply`
	- `git cherry-pick`
- Abortar merge y rebase
	- `git merge --abort`
	- `git rebase --abort`
- Cómo se ven los conflictos
- Merge versus rebase

-----------------
### Ejercicio 4: 
Copiar y pegar carpeta en otra ruta para duplicar el repositorio. En uno, hacer un merge entre 2 ramas y en el otro hacer un rebase.

-----------------
- Forks
	- Utilidad e historial
- Reglas y permisos de un repositorio
- Pull requests
	- Creating a PR
	- Elegir ramas de los forks para enviar
	- Aceptación de PC

-----------------
### Ejercicio 5: 
Un integrante hará un pull request y otro lo aceptará o rechazará. 

-----------------
- Stash
	- `git stash`
	- `git stash apply`
	- `git stash list`
	- `git stash apply N`
	- `git stash push -m "message"`
	- `git stash drop N`
	- `git stash pop`
	- `git stash clear` 
- Amend commit
	- `git commit --amend - "message"`

-----------------
### Ejercicio 6: 
Comenzar a trabajar en una funcionalidad ficticia y usar stash para guardar el WIP. Luego comitear y usar amend para corregir el commit.

-----------------

## Links relevantes

- [Git Internals - Git Objects](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects)
- [Where system, global and local Git config files on Windows and Ubuntu Linux are](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/Where-system-global-and-local-Windows-Git-config-files-are-saved)
- [Setting your username in Git](https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git)
- [Setting your commit email address](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)
- [Managing remote repositories](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories)
- [Git Basics - Git Aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)
- [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- ![Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk&ab_channel=freeCodeCamp.org)
- ![Git for Professionals Tutorial - Tools & Concepts for Mastering Version Control with Git](https://www.youtube.com/watch?v=Uszj_k0DGsg)
- ![Git Branches Tutorial](https://www.youtube.com/watch?v=e2IbNHi4uCI&ab_channel=freeCodeCamp.org)
- ![How to Undo Mistakes With Git Using the Command Line](https://www.youtube.com/watch?v=lX9hsdsAeTk&ab_channel=freeCodeCamp.org)
- ![Git STASH Explained in Simple Words](https://www.youtube.com/watch?v=DeU6opFU_zw&ab_channel=Academind)
- ![Advanced Git Tutorial - Interactive Rebase, Cherry-Picking, Reflog, Submodules and more](https://www.youtube.com/watch?v=qsTthZi23VE&ab_channel=freeCodeCamp.org)
- ![What MOST programmers don’t know about GIT?](https://www.youtube.com/watch?v=RxHJdapz2p0&ab_channel=TechWithNikola)
- ![Git Internals - The BLOB](https://www.youtube.com/watch?v=_wj4MGuvcjc&ab_channel=Ashotofcode)
- ![10 Must Know Git Commands That Almost Nobody Knows](https://www.youtube.com/watch?v=mnmYwRoSisg&ab_channel=WebDevSimplified)
- ![E13 - Cómo usar Git: Tutorial básico y buenas prácticas](https://www.youtube.com/watch?v=h0wSb2n7PkY&ab_channel=en_coders)
- ![21 alias útiles para git](https://elbauldelprogramador.com/21-aliases-utiles-para-git/)

## Volver al inicio

[[resumenes_clases_MDS7201]]