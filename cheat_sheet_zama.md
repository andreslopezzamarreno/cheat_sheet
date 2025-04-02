# 📝 Cheatsheet de Cosas Random

## Índice
- [Programación](#programacion)
- [Atajos de Teclado](#atajos-de-teclado)
  - [Windows](#windows)
  - [VS code](#visual-Studio-Code)
- [Comandos Útiles](#comandos-utiles)
  - [Git](#git)
- [Tips Variados](#tips-variados)
  - [Crear cualquier web como app Windows](#crear-cualquier-web-como-app-windows)
  - [Ejecutar cualquier script desde el arranque](#ejecutar-cualquier-script-desde-el-arranque)

---

## Programación
---

## Atajos de Teclado
### Windows
- `Win + D` → Mostrar escritorio
- `Alt + Tab` → Cambiar ventana

### Visual Studio Code
- `ctrl + j`→ ocultar/mostrar consola
- `shift + alt + a` → comentar/descomentar codigo de colpe (seleccionando texto)
---

## Comandos Útiles
### Git
```sh
git checkout rama  # Cambiar de rama
git pull  # Actualizar repo local con el remoto
git push  # Subir repo local al remoto
git commit -m "mensaje"  # Commit con mensaje
```

#### `.gitignore`
Ignora absolutamente todo lo que esté listado en este archivo y evita que se suba al repositorio.

---

## Tips Variados
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
1. Crear un acceso directo a un script de PowerShell que lance el archivo `.py`
2. Guardarlo en la carpeta de inicio (`shell:startup`)
3. Ejemplo de comando PowerShell:
```powershell
Start-Process python "C:\ruta\a\script.py"
```

---
