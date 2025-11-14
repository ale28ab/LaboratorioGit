#  Laboratorio Git — Comandos Fundamentales

## Comandos de Git explicados

### 1 `git add`
**Descripción:**  
Agrega archivos modificados o nuevos al área de preparación (*staging area*) para ser incluidos en el próximo commit.

**Ejemplo:**
```bash
git add README.md
````

**Salida esperada:**

```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md
```

### 2️ `git commit -m`

**Descripción:**
Registra los cambios añadidos con un mensaje descriptivo. Es uno de los comandos más usados en Git.

**Ejemplo:**

```bash
git commit -m "Agrego README con explicaciones de comandos"
```

**Salida esperada:**

```
[master (root-commit) d1a3c2b] Agrego README con explicaciones de comandos
 1 file changed, 10 insertions(+)
 create mode 100644 README.md
```


### 3 `git push`

**Descripción:**
Envía los commits locales al repositorio remoto (por ejemplo, GitHub).
Se usa normalmente junto con el nombre del remoto (`origin`) y la rama (`master` o `main`).

**Ejemplo:**

```bash
git push origin master
```

**Salida esperada:**

```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
To https://github.com/ale28ab/LaboratorioGit.git
```


### 4️ `git pull`

**Descripción:**
Descarga y fusiona los cambios del repositorio remoto al local, asegurando que ambos estén sincronizados.

**Ejemplo:**

```bash
git pull origin master
```

**Salida esperada:**

```
Already up to date.
```

### 5 `git rebase`

**Descripción:**
Permite mover o combinar commits de una rama sobre otra, manteniendo una historia más limpia y lineal.

**Ejemplo:**

```bash
git rebase master
```


### 6️ `git rebase -i HEAD~x`

**Descripción:**
Ejecuta un **rebase interactivo**, donde se pueden editar, combinar (`squash`) o renombrar (`reword`) los últimos commits.

**Ejemplo:**

```bash
git rebase -i HEAD~3
```



*Vista de commits seleccionados en modo interactivo.*


### 7️ `git status`

**Descripción:**
Muestra el estado actual del repositorio: qué archivos están modificados, nuevos o listos para hacer commit.

**Ejemplo:**

```bash
git status
```

**Salida esperada:**

```
On branch master
nothing to commit, working tree clean
```

### 8️ `git log`

**Descripción:**
Muestra el historial de commits con sus mensajes, autores y fechas.
El modo simplificado (`--oneline`) muestra una vista más compacta.

**Ejemplo:**

```bash
git log --oneline
```

### 9️ `git diff`

**Descripción:**
Muestra las diferencias entre archivos modificados y su última versión confirmada.

**Ejemplo:**

```bash
git diff README.md
```


### 10 `git branch`

**Descripción:**
Crea, lista o elimina ramas dentro del repositorio.

**Ejemplo:**

```bash
git branch pruebas_git
git branch
```

**Salida esperada:**

```
* master
  pruebas_git
```


### 11 `git branch -D`

**Descripción:**
Elimina una rama local de forma forzada, incluso si no ha sido fusionada.

**Ejemplo:**

```bash
git branch -D pruebas_git
```

### 12 `git checkout`

**Descripción:**
Permite cambiar de rama o restaurar archivos a un estado anterior.

**Ejemplo:**

```bash
git checkout master
```

---

### 13 `git commit --amend`

**Descripción:**
Modifica el último commit, permitiendo corregir su mensaje o agregar nuevos archivos.

**Ejemplo:**

```bash
git commit --amend -m "Actualizo mensaje del último commit"


### 14 `git commit --amend --no-edit`

**Descripción:**
Actualiza el último commit **sin cambiar su mensaje**, ideal para incluir pequeños cambios olvidados.

**Ejemplo:**

```bash
git add archivo.txt
git commit --amend --no-edit
```

Autor: Kevin Gutierrez
Repositorio: [LaboratorioGit](https://github.com/ale28ab/LaboratorioGit)
Colaborador: Alejandro Aguilar


