- [Markdown Cheat Sheet](#Markdown-Cheat-Sheet)
- [Encabezados](#Encabezados)
    - [Énfasis](#Énfasis)
    - [Listas No Ordenadas](#Listas-No-Ordenadas)
    - [Listas Ordenadas](#Listas-Ordenadas)
    - [Citas](#Citas)
    - [Bloques de Código](#Bloques-de-Código)
    - [Enlaces e Imágenes](#Enlaces-e-Imágenes)
    - [Tablas](#Tablas)
    - [Líneas Horizontales](#Líneas-Horizontales)
    - [Tablas](#Tablas)
    - [Tareas (Checkboxes)](#Tareas-(Checkboxes))


## Markdown Cheat Sheet
**Encabezados**
```markdown
# Título 1  
## Título 2  
### Título 3  
#### Título 4  
##### Título 5  
###### Título 6  
```
**Énfasis**
Pueden combinarse

```markdown
**Negrita** o __Negrita__  
*Cursiva* o _Cursiva_  
~~Tachado~~  
```
Ejemplo:
Esto es un texto **negro**, _cursivo_ ,~~tachado~~ **_~~negro, tachado y cursivo~~_**
**Listas No Ordenadas**
```markdown
- Elemento 1  
- Elemento 2  
  - Sub-elemento 1  
  - Sub-elemento 2  
* Elemento 3  
```
**Listas Ordenadas**
```markdown
1. Elemento 1  
2. Elemento 2  
  1. Sub-elemento 1  
  2. Sub-elemento 2  
3. Elemento 3  
```
**Citas**
```markdown
> Esto es una cita  
>> Esto es una cita anidada  
```
Se ve asi:
> Esto es una cita
>> esto es una cita a anidada

**Bloques de Código**
Sustituye "python" por practicamente cualquier lenguanje:
> javascript, java, c, cpp, csharp, kotlin, typescript, php, bash, html, xml, css, json, yaml, markdown, sql, graphql, powershell, makefile, dockerfile, plantuml
````
```python
# Bloque de código
print("¡Hola, Markdown!")
```
````
Se ve asi:
```python
# Bloque de código
print("¡Hola, Markdown!")
```
**Enlaces e Imágenes**
```markdown
[Texto del enlace](https://ejemplo.com)  
![Texto alternativo](https://ejemplo.com/imagen.jpg)  
![Texto alternativo](imagen.jpg) -> La foto tiene que estar en la carpeta indicada (no se puede copiar y pegar como en word)
```
**Tablas**
```markdown
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|--------------|--------------|--------------|
| Dato 1       | Dato 2       | Dato 3       |
| Dato 4       | Dato 5       | Dato 6       |
```
Se ve asi:
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|--------------|--------------|--------------|
| Dato 1       | Dato 2       | Dato 3       |
| Dato 4       | Dato 5       | Dato 6       |

**Líneas Horizontales**
```markdown
---
```
**Tareas (Checkboxes)**
```markdown
- [x] Tarea completada  
- [ ] Tarea pendiente  
```