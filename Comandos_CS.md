# 📝 Cheatsheet

---

## Índice

- [Git](#git)
- [Atajos de Teclado](#atajos-de-teclado)
  - [Windows](#windows)
  - [Chrome](#Chrome)
- [VS code](#visual-Studio-Code)
  - [Comandos](#Comandos)
  - [Extensiones](#Extensiones-interesantes)
- [Ejecutar cualquier script desde el arranque](#ejecutar-cualquier-script-desde-el-arranque)
- [Encender el portatil remotamente](#Encender-el-portatil-remotamente)
- [Raspberry Pi](#Raspberry-Pi)
- [Significado de Siglas/Acronimos y sus definiciones](#Significado-de-Siglas/Acronimos-y-sus-definiciones)

---

## Atajos de Teclado

### Windows

- `Win + D` → minimizar todas las ventanas (Mostrar escritorio)
- `Alt + Tab` → Cambiar ventana
- `win + m` → minimiza todas las ventanas
- `win + p` → configuracion pantallas
- `alt + f4` o `ctrl + alt + f4` → Cerrar aplicacion actual
- `Win + Shift + S` → Captura de pantalla

### Chrome

- `ctrl + t` → Abrir nueva ventana
- `ctrl + w` → Cerrar ventana actual
- `ctrl + tab` → saltar a ventana de la derecha
- `ctrl + r` → refrescar
- `ctrl + l` o `Alt + D` → Poner foco en la barra de busqueda
- `boton central` → cerrar ventana (poner raton sobre pestaña que se quiere cerrar)
- `ctrl + <numero>` → ir a pestaña que se le indique
- `shift + alt + b` → ocultar/mostrar marcadores

---


## Visual Studio Code

### Comandos

- `ctrl + j`→ ocultar/mostrar consola
- `shift + alt + a` → comentar/descomentar codigo de colpe (seleccionando texto)
- Autoguardado
  - file > preferences > settings
  - buacar `files.autoSave`
  - seleccionar `afterDelay`
- `ctrl + shift + c` → abrir consolar cmd con la ruta de la carpeta
- `boton central` → cerrar ventana (poner raton sobre pestaña que se quiere cerrar)
- `ctrl + p` → Abrir buscador de archivos
- `shift + alt + f` → Formatear al codigo de fo

### Extensiones-interesantes

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

##### Combinar comandos

Usar "&&"
Ejemplo:

```sh
git commit -a -m "Mensaje" && git push #Add, commit y push todo en un comando
```

#### `.gitignore`

Ignora absolutamente todo lo que esté listado en este archivo y evita que se suba al repositorio.

---

## Ejecutar cualquier script desde el arranque

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

---

## Encender el portatil remotamente

Requisitos:

- wake on LAN disponible en el ordenador
- Cable de red siempre conectado
- Otro ordenador en casa siempre conectado (servidor local, raspberry, ordenador antiguo...)

por hacer

---

## Raspberry Pi

### Conectarme por SSH en windows
  - Conectar raspberry por cable
  - Instalar putty en windows
  - usar Fing para escanear tu red local desde el móvil para encontrar ip local
  - conectarme por putty a esa ip con usaurio y contraseña

### Configurar wifi

### Instalar docker en Raspberry pi

### Crear contenedor docker

### Crear vpn con Raspberry
  - instalar WireGuard en el movil
  
### Encender el ordenador desde fuera de casa
  - usar WOL (wake on lan ) -> no disponible en mi ordenador

---

## Significado de Siglas/Acronimos y sus definiciones

- `VPN` → Virtual Private Network

  - ¿Para qué sirve?
    Permite establecer una conexión segura y cifrada entre el usuario y una red a través de Internet. Se utiliza para proteger la privacidad en línea, acceder a contenidos restringidos geográficamente y mantener la seguridad en redes públicas.

- `Protocolo de Red`

  - ¿Para qué sirve?
    Los protocolos de red permiten que computadoras, servidores, routers y otros dispositivos intercambien datos de manera eficiente y segura. Establecen cómo se inician, mantienen y terminan las conexiones, así como el formato de los datos transmitidos. Ejemplos de protocolos de red incluyen IP, TCP, HTTP, FTP, y SSH.

- `IP` → Internet Protocol

  - ¿Para qué sirve?
    Es el conjunto de reglas que rige cómo se enrutan y direccionan los datos a través de redes para que lleguen al destino correcto. Cada dispositivo conectado a una red tiene una dirección IP que lo identifica de manera única.

- `SSH` → Secure Shell
  - ¿Para qué sirve?
    SSH es un protocolo de red que permite acceder de forma segura a otro dispositivo a través de una red no segura, como Internet. Se usa principalmente para administrar servidores de forma remota mediante una línea de comandos cifrada, protegiendo la información transmitida frente a posibles interceptaciones.
- `TCP` → Transmission Control Protocol

  - ¿Para qué sirve?
    Es uno de los protocolos fundamentales del conjunto de protocolos de Internet. TCP se encarga de garantizar que los datos enviados desde un dispositivo lleguen correctamente y en orden al dispositivo de destino. Ofrece una transmisión de datos confiable, controlando errores y gestionando la fragmentación y reensamblaje de los datos.

- `HTTP` → HyperText Transfer Protocol

  - ¿Para qué sirve?
    Es el protocolo que permite la comunicación entre navegadores web y servidores. Se usa para cargar páginas web y transmitir contenido como texto, imágenes, y otros datos multimedia a través de Internet. No cifra la información, por lo que no es seguro para el envío de datos sensibles.

- `HTTPS` → HyperText Transfer Protocol Secure

  - ¿Para qué sirve?
    Es la versión segura de HTTP. Utiliza cifrado mediante TLS (anteriormente SSL) para proteger la información que se transmite entre el navegador y el servidor. Se emplea en sitios web que manejan datos sensibles, como contraseñas, tarjetas de crédito o información personal.

- `TLS` → Transport Layer Security

  - ¿Para qué sirve?
    TLS es un protocolo criptográfico que proporciona privacidad e integridad en las comunicaciones a través de Internet. Se usa principalmente para cifrar conexiones como HTTPS, correo electrónico, mensajería instantánea y llamadas VoIP. TLS asegura que los datos transmitidos no puedan ser vistos ni modificados por terceros durante el tránsito.

- `DNS` → Domain Name System

  - ¿Para qué sirve?
    El DNS traduce nombres de dominio fáciles de recordar (como `www.ejemplo.com`) en direcciones IP numéricas que las computadoras usan para identificarse entre sí en la red. Es como una "agenda telefónica" de Internet. Sin DNS, tendrías que recordar direcciones IP en lugar de nombres de sitios web.

- `FTP` → File Transfer Protocol
  - ¿Para qué sirve?
    FTP es un protocolo utilizado para transferir archivos entre un servidor y un cliente a través de una red, como Internet. Permite subir o descargar archivos de manera eficiente y es muy utilizado en la administración de sitios web o en la compartición de grandes volúmenes de datos. FTP puede usar conexiones no cifradas (FTP) o cifradas (FTPS).

---
