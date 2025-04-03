# 📝 Cheatsheet

## Índice
- [Git](#git)
- [Atajos de Teclado](#atajos-de-teclado)
  - [Windows](#windows)
  - [VS code](#visual-Studio-Code)
    - [Extensiones](#Extensiones-interesantes)
- [Tips Variados](#tips-variados)
  - [Crear cualquier web como app Windows](#crear-cualquier-web-como-app-windows)
  - [Ejecutar cualquier script desde el arranque](#ejecutar-cualquier-script-desde-el-arranque)
  - [Enviar libro a ebook por correo](#Enviar-libro-a-ebook-por-correo)
  - [Sacar @clave](#Sacar-@clave)
---

## Atajos de Teclado
### Windows
- `Win + D` → Mostrar escritorio
- `Alt + Tab` → Cambiar ventana 


### Visual Studio Code
- `ctrl + j`→ ocultar/mostrar consola
- `shift + alt + a` → comentar/descomentar codigo de colpe (seleccionando texto)
- Autoguardado 
  - file > preferences > settings
  - buacar `files.autoSave`
  - seleccionar `afterDelay`
- `ctrl + shift + c` → abrir consolar cmd con la ruta de la carpeta 

  #### Extensiones-interesantes
  - Markdown Preview Enhanced 
    - `ctrl + shift + v` → abrir preview de markdown
  - Prettier - Code formatter 
  - Rainbow CSV 
    - Coloreado de un CSV
  - GitLens — Git supercharged
  - Excel Viewer 
    - Visor de excel en VSCode
  - Commit Message Editor
    - para mensajes de commit standard
  - SQLite Viewer 
    - visor de BBDD sql

---

## Comandos Útiles
### Git
##### Inicializar y Clonar Repositorios
```sh
git clone URL_REPO  # Clonar un repositorio remoto
git clone URL_REPO nombre_directorio  # Clonar en un directorio específico
```
##### Estados y Cambios
```sh
git status  # Ver estado de los archivos en el repositorio
git add archivo  # Agregar archivo al staging area
git add .  # Agregar TODOS los archivos al staging area
git reset archivo  # Quitar archivo del staging sin borrar cambios
git reset --hard  # Eliminar todos los cambios no confirmados
git diff  # Ver diferencias entre archivos modificados y el último commit
git diff --staged  # Ver diferencias entre el staging area y el último commit
```
##### Commits
```sh
git commit -m "Mensaje"  # Guardar cambios con mensaje
git commit --amend -m "Nuevo mensaje"  # Editar el último commit
git commit -a -m "Mensaje"  # Hacer commit de todos los cambios rastreados
```
##### Ramas
```sh
git branch  # Listar ramas
git branch nueva_rama  # Crear nueva rama
git checkout rama  # Cambiar de rama
git checkout -b nueva_rama  # Crear y cambiar a una nueva rama
git branch -d rama  # Eliminar rama (solo si no tiene cambios sin fusionar)
git branch -D rama  # Forzar eliminación de rama
```
##### Actualizar y Subir Cambios
```sh
git pull  # Obtener cambios del remoto y fusionarlos
git pull --rebase  # Obtener cambios y rebasear
git push  # Subir cambios al repositorio remoto
git push -u origin rama  # Subir rama actual y establecer upstream
```
##### Fusionar y Rebasear
```sh
git merge rama  # Fusionar 'rama' con la actual
git merge --no-ff rama  # Fusionar sin fast-forward
git rebase rama  # Reaplicar commits sobre otra rama
git rebase --abort  # Cancelar un rebase en curso
git rebase --continue  # Continuar un rebase después de resolver conflictos
```
##### Revertir Cambios
```sh
git checkout archivo  # Restaurar un archivo modificado al último commit
git checkout -- .  # Restaurar todos los archivos modificados
git reset HEAD archivo  # Quitar archivo del staging
git reset --hard HEAD  # Deshacer todos los cambios locales
git revert HASH  # Crear un commit que revierte un cambio específico
```
##### Historial
```sh
git log  # Ver historial de commits
git log --oneline  # Ver historial resumido
git log --graph --decorate --oneline --all  # Ver historial con gráfico de ramas
git show HASH  # Ver detalles de un commit específico
```
#### `.gitignore`
Ignora absolutamente todo lo que esté listado en este archivo y evita que se suba al repositorio.

---

# Tips Variados
### Crear cualquier web como app Windows
1. Abrir Google Chrome
2. Ir al sitio que quieras instalar como app
3. Clic en los tres puntos del menú
4. Seleccionar "Enviar, guardar y compartir"
5. Click en "Instalar página como aplicación"

### Ejecutar cualquier script desde el arranque
1. `Win + R`
2. Escribir `shell:startup`
3. Pegar en la carpeta que se abre el script

#### Para Python:
  - por hacer
1. Crear un acceso directo a un script de PowerShell que lance el archivo `.py`
2. Guardarlo en la carpeta de inicio (`shell:startup`)
3. Ejemplo de comando PowerShell:
```powershell
Start-Process python "C:\ruta\a\script.py"
```
### Enviar libro a ebook por correo
  - por hacer
1. Ir a tres puntos configuracion
2. abajo del todo habra un correo
3. Enviar correo normal, no hace falta ni concepto ni nada
4. adjuntar archivo y enviar
5. esperar un par de minutos hasta que el libro salga en el menu del ebook

### Sacar @clave
  - por hacer
---