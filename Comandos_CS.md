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
- [Automatizar whatsapp con python](#automatizar-whatsapp-con-python)
- [Docker](#Docker)
- [WSL](#WSL)

---

## Atajos de Teclado

### Windows

- `Win + D`                       → minimizar todas las ventanas (Mostrar escritorio)
- `Alt + Tab`                     → Cambiar ventana
- `win + m`                       → minimiza todas las ventanas
- `win + p`                       → configuracion pantallas
- `alt + f4` o `ctrl + alt + f4`  → Cerrar aplicacion actual
- `Win + Shift + S`               → Captura de pantalla
- `Win + D`                       → minimizar todas las ventanas (Mostrar escritorio)
- `Alt + Tab`                     → Cambiar ventana
- `win + m`                       → minimiza todas las ventanas
- `win + p`                       → configuracion pantallas
- `alt + f4` o `ctrl + alt + f4`  → Cerrar aplicacion actual
- `Win + Shift + S`               → Captura de pantalla

### Chrome

- `ctrl + t`   → Abrir nueva ventana
- `ctrl + w`   → Cerrar ventana actual
- `ctrl + t`   → Abrir nueva ventana
- `ctrl + w`   → Cerrar ventana actual
- `ctrl + tab` → saltar a ventana de la derecha
- `ctrl + r`   → refrescar
- `ctrl + l` o `Alt + D` → Poner foco en la barra de busqueda
- `boton central`   → cerrar ventana (poner raton sobre pestaña que se quiere cerrar)
- `ctrl + <numero>` → ir a pestaña que se le indique
- `shift + alt + b` → ocultar/mostrar marcadores

---


## Visual Studio Code

  ### Comandos
  ### Comandos

  - `ctrl + j`        → ocultar/mostrar consola
  - `shift + alt + a` → comentar/descomentar codigo de colpe (seleccionando texto)
  - Autoguardado
    - file > preferences > settings
    - buacar `files.autoSave`
    - seleccionar `afterDelay`
  - `ctrl + shift + c` → abrir consolar cmd con la ruta de la carpeta
  - `boton central`    → cerrar ventana (poner raton sobre pestaña que se quiere cerrar)
  - `ctrl + p`         → Abrir buscador de archivos
  - `shift + alt + f`  → Formatear al codigo de fo

  ### Extensiones-interesantes
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

Usar `;`
Usar `;`
Ejemplo:

```sh
git add .; git commit -m "actualizacion cheat sheet"; git push #Add, commit y push todo en un comando
git add .; git commit -m "actualizacion cheat sheet"; git push #Add, commit y push todo en un comando
```

#### `.gitignore`

Ignora absolutamente todo lo que esté listado en este archivo y evita que se suba al repositorio.

---

## Ejecutar cualquier script desde el arranque

  1. `Win + R`
  2. Escribir `shell:startup`
  3. Pegar en la carpeta que se abre el script
  1. `Win + R`
  2. Escribir `shell:startup`
  3. Pegar en la carpeta que se abre el script

  #### Para 
  Python:
    - por hacer

    1. Crear un acceso directo a un script de PowerShell que lance el archivo `.py`
    2. Guardarlo en la carpeta de inicio (`shell:startup`)
    3. Ejemplo de comando PowerShell:

    ```powershell
    Start-Process python "C:\ruta\a\script.py"
    ```
  

## Encender el portatil remotamente

  Requisitos:
  Requisitos:

  - wake on LAN disponible en el ordenador
  - Cable de red siempre conectado
  - Otro ordenador en casa siempre conectado (servidor local, raspberry, ordenador antiguo...)

  por hacer
  por hacer

---

## Raspberry Pi
  ### Conectarme por SSH en windows
    - Conectar raspberry por cable
    - Instalar putty en windows
    - usar Fing para escanear tu red local desde el móvil para encontrar ip local
    - conectarme por putty a esa ip con usaurio y contraseña
  ### Conectarme por SSH en windows
    - Conectar raspberry por cable
    - Instalar putty en windows
    - usar Fing para escanear tu red local desde el móvil para encontrar ip local
    - conectarme por putty a esa ip con usaurio y contraseña

  ### Configurar wifi

  ### Instalar docker en Raspberry pi
  ### Instalar docker en Raspberry pi

  ### Crear contenedor docker
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


## Automatizar whatsapp con python

  ### A tu propio numero
    - mejor opcion  Callmebot
    - [Call me bot api](https://www.callmebot.com/blog/free-api-whatsapp-messages/)
    - Ejemplo en github [enlace github]()

    ### A otro numero/grupo
      - Ultramsg
      - Ejemplo en 

## Tener copia de google fotos en local

  ### Google takeout
    - Ir a [Google takeout](https://takeout.google.com/)
    - Dale a desmarcar todo, y baja hasta encontrar google fotos y selecciona.
    - Puedes seleccionar todo lo que quieras descargar
    - baja hasta abajo del todo y dale `siguiente paso`
    - `Destino` → `Enviar enlace de descarga por correo electronico`
    - `Frecuencia` → `Exportar cada 2 meses durante 1 año` o `Exportar una vez` si solo quieres una vez
    - `Tipo y tamaño de archivo` → `.ZIP` y el tamaño da un poco igual
    - Darle a `Crear exportacion`
    Esto hace que cada dos meses llegue un correo con los enlaces para descargarlo localmente

  ### Automatizar la descarga local
    - Pasos para hacerlo en una raspberry pero realmente se puede hacer en cualquier parte
    - pasos en [Repo G-Fotos](https://github.com/andreslopezzamarreno/automatizacion-fotos)

---

## Docker

  ### Conceptos básicos

  - **Docker** permite crear, desplegar y ejecutar aplicaciones en contenedores ligeros y portables.
  - Un **contenedor** es una instancia de una imagen que se ejecuta de forma aislada.
  - Una **imagen** es una plantilla inmutable con todo lo necesario para ejecutar una aplicación.

---

  ### Comandos útiles de Docker

  - **Ver versión de Docker instalada**
    ```sh
    docker --version
    ```

  - **Listar contenedores**
    - Activos:  
      ```sh
      docker ps
      ```
    - Todos (incluidos detenidos):  
      ```sh
      docker ps -a
      ```

  - **Listar imágenes**
    ```sh
    docker images
    ```

  - **Descargar una imagen**
    ```sh
    docker pull nombre_imagen
    ```

  - **Crear y ejecutar un contenedor**
    ```sh
    docker run -d --name mi_contenedor -p 8080:80 nombre_imagen
    ```
    - `-d`: modo "detached" (en segundo plano)
    - `--name`: nombre personalizado
    - `-p`: mapea puertos (host:contenedor)

  - **Entrar en un contenedor en ejecución**
    ```sh
    docker exec -it mi_contenedor bash
    ```

  - **Detener un contenedor**
    ```sh
    docker stop mi_contenedor
    ```

  - **Eliminar un contenedor**
    ```sh
    docker rm mi_contenedor
    ```

  - **Eliminar una imagen**
    ```sh
    docker rmi nombre_imagen
    ```

  - **Ver logs de un contenedor**
    ```sh
    docker logs mi_contenedor
    ```

  - **Construir una imagen desde un Dockerfile**
    ```sh
    docker build -t mi_imagen .
    ```

  - **Copiar archivos entre host y contenedor**
    - Del host al contenedor:
      ```sh
      docker cp archivo.txt mi_contenedor:/ruta/destino/
      ```
    - Del contenedor al host:
      ```sh
      docker cp mi_contenedor:/ruta/origen/archivo.txt ./
      ```

  - **Limpiar recursos no usados**
    ```sh
    docker system prune
    ```

---

  ### Notas útiles

  - Para ver información detallada de un contenedor:
    ```sh
    docker inspect mi_contenedor
    ```
  - Para ver el uso de espacio:
    ```sh
    docker system df
    ```
  - Puedes usar `docker-compose` para gestionar varios contenedores con un solo archivo `docker-


## Automatizar whatsapp con python

  ### A tu propio numero
    - mejor opcion  Callmebot
    - [Call me bot api](https://www.callmebot.com/blog/free-api-whatsapp-messages/)
    - Ejemplo en github [enlace github]()

    ### A otro numero/grupo
      - Ultramsg
      - Ejemplo en 

## Tener copia de google fotos en local

  ### Google takeout
    - Ir a [Google takeout](https://takeout.google.com/)
    - Dale a desmarcar todo, y baja hasta encontrar google fotos y selecciona.
    - Puedes seleccionar todo lo que quieras descargar
    - baja hasta abajo del todo y dale `siguiente paso`
    - `Destino` → `Enviar enlace de descarga por correo electronico`
    - `Frecuencia` → `Exportar cada 2 meses durante 1 año` o `Exportar una vez` si solo quieres una vez
    - `Tipo y tamaño de archivo` → `.ZIP` y el tamaño da un poco igual
    - Darle a `Crear exportacion`
    Esto hace que cada dos meses llegue un correo con los enlaces para descargarlo localmente

  ### Automatizar la descarga local
    - Pasos para hacerlo en una raspberry pero realmente se puede hacer en cualquier parte
    - pasos en [Repo G-Fotos](https://github.com/andreslopezzamarreno/automatizacion-fotos)

---

## Docker

  ### Conceptos básicos

  - **Docker** permite crear, desplegar y ejecutar aplicaciones en contenedores ligeros y portables.
  - Un **contenedor** es una instancia de una imagen que se ejecuta de forma aislada.
  - Una **imagen** es una plantilla inmutable con todo lo necesario para ejecutar una aplicación.

---

  ### Comandos útiles de Docker

  - **Ver versión de Docker instalada**
    ```sh
    docker --version
    ```

  - **Listar contenedores**
    - Activos:  
      ```sh
      docker ps
      ```
    - Todos (incluidos detenidos):  
      ```sh
      docker ps -a
      ```

  - **Listar imágenes**
    ```sh
    docker images
    ```

  - **Descargar una imagen**
    ```sh
    docker pull nombre_imagen
    ```

  - **Crear y ejecutar un contenedor**
    ```sh
    docker run -d --name mi_contenedor -p 8080:80 nombre_imagen
    ```
    - `-d`: modo "detached" (en segundo plano)
    - `--name`: nombre personalizado
    - `-p`: mapea puertos (host:contenedor)

  - **Entrar en un contenedor en ejecución**
    ```sh
    docker exec -it mi_contenedor bash
    ```

  - **Detener un contenedor**
    ```sh
    docker stop mi_contenedor
    ```

  - **Eliminar un contenedor**
    ```sh
    docker rm mi_contenedor
    ```

  - **Eliminar una imagen**
    ```sh
    docker rmi nombre_imagen
    ```

  - **Ver logs de un contenedor**
    ```sh
    docker logs mi_contenedor
    ```

  - **Construir una imagen desde un Dockerfile**
    ```sh
    docker build -t mi_imagen .
    ```

  - **Copiar archivos entre host y contenedor**
    - Del host al contenedor:
      ```sh
      docker cp archivo.txt mi_contenedor:/ruta/destino/
      ```
    - Del contenedor al host:
      ```sh
      docker cp mi_contenedor:/ruta/origen/archivo.txt ./
      ```

  - **Limpiar recursos no usados**
    ```sh
    docker system prune
    ```

---

  ### Notas útiles

  - Para ver información detallada de un contenedor:
    ```sh
    docker inspect mi_contenedor
    ```
  - Para ver el uso de espacio:
    ```sh
    docker system df
    ```
  - Puedes usar `docker-compose` para gestionar varios contenedores con un solo archivo `docker-

## WSL
  - apagar wsl desde cmd --> wsl --shutdown
  - cd ~ -> ir a directorio raiz

---

## Comandos TOP Windows (que nadie conoce)

### Abrir aplicaciones desde CMD/PowerShell
- `code .` → Abrir VS Code en la carpeta actual
- `notepad archivo.txt` → Crear y abrir archivo en Notepad
- `start .` → Abrir explorador en la carpeta actual
- `explorer .` → Igual que start pero más directo
- `calc` → Abrir calculadora
- `mspaint` → Abrir Paint
- `winver` → Ver versión de Windows
- `msinfo32` → Información completa del sistema
- `dxdiag` → Diagnóstico DirectX

### Comandos desde "Ejecutar" (Win + R)
- `shell:startup` → Carpeta de inicio automático
- `shell:sendto` → Carpeta "Enviar a"
- `shell:recent` → Archivos recientes
- `shell:downloads` → Carpeta de descargas
- `%temp%` → Carpeta temporal (para limpiar)
- `%appdata%` → Datos de aplicaciones
- `cleanmgr` → Limpiador de disco
- `resmon` → Monitor de recursos avanzado
- `perfmon` → Monitor de rendimiento
- `devmgmt.msc` → Administrador de dispositivos

### Atajos de teclado secretos
- `Win + V` → Historial del portapapeles (si está habilitado)
- `Win + .` → Panel de emojis 😊
- `Win + ;` → Panel de emojis (alternativo)
- `Win + H` → Dictado por voz
- `Win + Ctrl + D` → Crear escritorio virtual nuevo
- `Win + Ctrl + F4` → Cerrar escritorio virtual actual
- `Win + Ctrl + ←/→` → Cambiar entre escritorios virtuales
- `Alt + F4` → Cerrar ventana actual
- `Win + I` → Configuración de Windows
- `Win + X` → Menú de herramientas de administración
- `Win + G` → Xbox Game Bar (grabar pantalla)
- `Win + K` → Conectar dispositivos inalámbricos
- `Win + U` → Centro de accesibilidad

### Comandos avanzados CMD/PowerShell
- `ipconfig /all` → Información completa de red
- `ipconfig /flushdns` → Limpiar caché DNS
- `sfc /scannow` → Escanear archivos del sistema
- `chkdsk C: /f` → Verificar disco duro (requiere reinicio)
- `tasklist` → Ver todos los procesos
- `taskkill /im proceso.exe /f` → Matar proceso por nombre
- `systeminfo` → Información detallada del sistema
- `netstat -an` → Ver conexiones de red activas
- `powercfg /batteryreport` → Reporte de batería (laptops)
- `tree` → Mostrar estructura de carpetas en árbol

### Trucos del explorador de archivos
- Escribir en la barra de direcciones:
  - `cmd` → Abrir CMD en esa carpeta
  - `powershell` → Abrir PowerShell en esa carpeta
  - `wt` → Abrir Windows Terminal (si está instalado)
- `F2` → Renombrar archivo seleccionado
- `F5` → Actualizar carpeta
- `Ctrl + Shift + N` → Nueva carpeta
- `Alt + ↑` → Subir un nivel de carpeta
- `Ctrl + L` → Seleccionar barra de direcciones

### Comandos para gestión de archivos
- `attrib +h archivo.txt` → Ocultar archivo
- `attrib -h archivo.txt` → Mostrar archivo oculto
- `copy con archivo.txt` → Crear archivo desde CMD (Ctrl+Z para terminar)
- `type archivo.txt` → Mostrar contenido de archivo
- `dir /ah` → Mostrar solo archivos ocultos
- `xcopy origen destino /s /e` → Copiar carpetas completas

### Comandos de red súper útiles
- `ping google.com` → Probar conexión
- `nslookup google.com` → Resolver DNS
- `tracert google.com` → Trazar ruta de red
- `netsh wlan show profiles` → Ver redes WiFi guardadas
- `netsh wlan show profile "NOMBRE_RED" key=clear` → Ver contraseña WiFi guardada

### Trucos con fechas y hora
- `date /t` → Mostrar fecha actual
- `time /t` → Mostrar hora actual
- `echo %date%` → Mostrar fecha en variable
- `echo %time%` → Mostrar hora en variable