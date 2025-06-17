# 📝 Cheatsheet

---

## Índice

- [C avanzado](#c-avanzado)

---

## C avanzado

### Conceptos

- **Puntero**: Variable que almacena la dirección de memoria de otra variable.
    - Declaración: `int *p;`
    - Obtener dirección: `p = &variable;`
    - Acceder al valor: `*p`
    - Ejemplo:
      ```c
      int x = 10;
      int *p = &x;
      printf("%d", *p); // Imprime 10
      ```
- **Array**: Conjunto de elementos del mismo tipo almacenados en posiciones contiguas de memoria.
    - Declaración: `int arr[5];`
    - Acceso: `arr[0] = 1;`

---

### Métodos y funciones estándar

- **printf()**: Imprime texto en pantalla.
    - Ejemplo: `printf("Hola %d", 5);`
- **puts()**: Imprime una cadena y añade salto de línea.
    - Ejemplo: `puts("Hola");`
- **putchar()**: Imprime un solo carácter.
    - Ejemplo: `putchar('A');`
- **scanf()**: Lee datos desde teclado.
    - Ejemplo: `scanf("%d", &x);`
- **getchar()**: Lee un carácter del teclado.
    - Ejemplo: `char c = getchar();`
- **gets()**: Lee una línea de texto (¡No recomendado por inseguro!).
    - Mejor usar `fgets()`.
- **fgets()**: Lee una línea de texto de forma segura.
    - Ejemplo: `fgets(buffer, sizeof(buffer), stdin);`

#### Funciones de manipulación de cadenas (`string.h`)

- **strlen(cad)**: Devuelve la longitud de la cadena.
    - Ejemplo: `int l = strlen("hola"); // l = 4`
- **strcpy(dest, orig)**: Copia una cadena en otra.
    - Ejemplo: `strcpy(dest, orig);`
- **strcat(dest, orig)**: Concatena dos cadenas.
    - Ejemplo: `strcat(dest, orig);`
- **strcmp(cad1, cad2)**: Compara dos cadenas.
    - Devuelve 0 si son iguales, <0 si cad1<cad2, >0 si cad1>cad2.
- **strchr(cad, c)**: Busca un carácter en una cadena.
    - Devuelve un puntero a la primera aparición o NULL.
- **strstr(cad, sub)**: Busca una subcadena en una cadena.
    - Devuelve un puntero al inicio de la subcadena o NULL.

---

### Registros (struct)

- Permiten agrupar diferentes tipos de datos bajo un mismo nombre.
- Ejemplo:
  ```c
  typedef struct {
      int id;
      char nombre[50];
      float salario;
  } Empleado;

  Empleado e1;
  e1.id = 1;
  strcpy(e1.nombre, "Juan");
  e1.salario = 1000.0;
  ```
- Son similares a las clases pero sin métodos.

---

### Arrays dinámicos

- Permiten reservar memoria en tiempo de ejecución.
- **malloc()**: Reserva memoria.
    - Ejemplo: `int *arr = (int*) malloc(n * sizeof(int));`
- **free()**: Libera memoria reservada.
    - Ejemplo: `free(arr);`
- **calloc()**: Igual que malloc pero inicializa a cero.
    - Ejemplo: `int *arr = (int*) calloc(n, sizeof(int));`
- **realloc()**: Cambia el tamaño de un bloque de memoria.
    - Ejemplo: `arr = (int*) realloc(arr, nuevo_tam * sizeof(int));`

---

### Control de flujo

- **if / else**:
  ```c
  if (condición) {
      // código
  } else {
      // otro código
  }
  ```
- **switch**:
  ```c
  switch (opcion) {
      case 1: /* ... */ break;
      case 2: /* ... */ break;
      default: /* ... */
  }
  ```
- **for**:
  ```c
  for (int i = 0; i < n; i++) { /* ... */ }
  ```
- **while / do-while**:
  ```c
  while (condición) { /* ... */ }
  do { /* ... */ } while (condición);
  ```

---

### Funciones

- Declaración y uso:
  ```c
  int suma(int a, int b) {
      return a + b;
  }
  int main() {
      int r = suma(2, 3);
      printf("%d", r);
      return 0;
  }
  ```

---

### Tipos de datos

- Básicos: `int`, `float`, `double`, `char`
- Modificadores: `short`, `long`, `unsigned`, `signed`
- Ejemplo: `unsigned long int x;`

---

### Operadores

- Aritméticos: `+`, `-`, `*`, `/`, `%`
- Relacionales: `==`, `!=`, `<`, `>`, `<=`, `>=`
- Lógicos: `&&`, `||`, `!`
- Asignación: `=`, `+=`, `-=`, etc.
- Incremento/Decremento: `++`, `--`

---

### Entrada/Salida

- **printf()**, **scanf()**: Entrada y salida estándar.
- **gets()**, **fgets()**, **puts()**, **putchar()**: Para cadenas y caracteres.
- Ejemplo:
  ```c
  char nombre[50];
  printf("Introduce tu nombre: ");
  fgets(nombre, 50, stdin);
  printf("Hola %s", nombre);
  ```

---

### Compilación

- Compilar un archivo:
  ```sh
  gcc archivo.c -o programa
  ./programa
  ```
- Compilar con depuración:
  ```sh
  gcc -g archivo.c -o programa
  ```

---

### Notas útiles

- Siempre liberar la memoria reservada con `free()`.
- Evitar `gets()`, usar `fgets()` para evitar desbordamientos.
- Usar `const` para parámetros que no deben modificarse.
- Los arrays en C empiezan en índice 0.
- Los strings terminan en `\0` (carácter nulo).

---

## Más datos útiles de C

### Booleanos en C

- C no tiene un tipo `bool` nativo en ANSI C.
- Se suele usar `int` (0 = falso, distinto de 0 = verdadero).
- Desde C99 puedes usar:
  ```c
  #include <stdbool.h>
  bool bandera = true;
  ```
- Valores posibles: `true` y `false`.

---

### Constantes

- Usa `#define` para constantes:
  ```c
  #define PI 3.1416
  ```
- O usa `const`:
  ```c
  const int max = 100;
  ```

---

### Enumeraciones (enum)

- Permiten definir conjuntos de constantes con nombre:
  ```c
  enum Color { ROJO, VERDE, AZUL };
  enum Color c = ROJO;
  ```

---

### Macros

- Son instrucciones que se expanden antes de compilar:
  ```c
  #define CUADRADO(x) ((x)*(x))
  ```

---

### Preprocesador

- Instrucciones que empiezan con `#`:
  - `#include <stdio.h>`
  - `#define`
  - `#ifdef`, `#ifndef`, `#endif`

---

### Comentarios

- Una línea: `// comentario`
- Varias líneas:
  ```c
  /* comentario
     de varias líneas */
  ```

---

### Alcance de variables

- Variables locales: declaradas dentro de funciones o bloques `{}`.
- Variables globales: declaradas fuera de cualquier función.
- Variables estáticas: `static int x;` mantienen su valor entre llamadas.

---

### Paso de argumentos a funciones

- Por valor: se pasa una copia.
- Por referencia: se pasa la dirección usando punteros.

---

### Archivos

- Para leer y escribir archivos:
  ```c
  FILE *f = fopen("archivo.txt", "r");
  fprintf(f, "Hola");
  fclose(f);
  ```

---

### Salida de error

- Usa `stderr` para imprimir errores:
  ```c
  fprintf(stderr, "Error: archivo no encontrado\n");
  ```

---

### Salida de un programa

- Usa `return 0;` para indicar éxito.
- Usa `return 1;` (u otro valor distinto de 0) para indicar error.

---

### Orden de evaluación

- El orden de evaluación de los argumentos de una función no está definido.
- Evita expresiones con efectos secundarios en los argumentos.

---

### Null pointer

- El puntero nulo es `NULL`.
  ```c
  int *p = NULL;
  ```

---

### Casting

- Para convertir tipos:
  ```c
  double x = (double) 5 / 2; // x = 2.5
  ```

---