---
sidebar_position: 2
---

### Investigación sobre la estructura de un programa en C

Un programa en C típicamente se compone de las siguientes partes:
1. **Directivas de preprocesador**: Incluyen las librerías necesarias para el programa (`#include`).
2. **Definiciones de constantes y macros**: Utilizan `#define` para definir constantes.
3. **Declaraciones de variables globales**: Variables accesibles desde cualquier parte del programa.
4. **Prototipos de funciones**: Declaraciones de funciones antes de su implementación.
5. **Función `main`**: Punto de entrada del programa.
6. **Implementación de funciones**: Definición de funciones utilizadas en el programa.

### ¿Qué son librerías?

Las librerías en C son colecciones de funciones y definiciones que facilitan la programación, permitiendo reutilizar código preescrito y probadamente funcional. Las librerías estándar de C incluyen funciones para manejar entradas y salidas, manipulación de cadenas, matemáticas, etc.

### ¿Cómo se declaran las librerías?

Las librerías se incluyen en un programa C usando la directiva `#include`. Por ejemplo, para incluir la librería estándar de entrada y salida:
```c
#include <stdio.h>
```

### ¿Cuáles son las librerías básicas?

Algunas de las librerías básicas en C son:
- `<stdio.h>`: Para entrada y salida estándar.
- `<stdlib.h>`: Para funciones de utilidad general, gestión de memoria, control de procesos, etc.
- `<string.h>`: Para manipulación de cadenas.
- `<math.h>`: Para funciones matemáticas.
- `<ctype.h>`: Para funciones de clasificación y conversión de caracteres.

### ¿Por qué son .h?

Las librerías en C se declaran con la extensión `.h` (de "header" o encabezado) porque contienen declaraciones de funciones, macros y variables que pueden ser compartidas entre múltiples archivos fuente. Estos archivos encabezados se incluyen en los programas con la directiva `#include`.

### ¿Qué es una variable?

Una variable es un espacio de memoria identificado por un nombre, que almacena un valor que puede cambiar durante la ejecución del programa. En C, las variables deben ser declaradas antes de ser usadas.

### ¿Qué es una variable local?

Una variable local es aquella que se declara dentro de una función y solo puede ser usada dentro de esa función. Su alcance es limitado al bloque de código donde fue definida.

### ¿Qué es una variable global?

Una variable global se declara fuera de todas las funciones, generalmente al principio del archivo fuente, y puede ser utilizada por cualquier función en el programa. Su alcance es todo el programa.

### Diferencias entre variables locales y globales y su uso

- **Variables locales**:
  - Alcance limitado a la función o bloque donde se declaran.
  - No interfieren con variables del mismo nombre en otras funciones.
- **Variables globales**:
  - Alcance en todo el programa.
  - Pueden ser accedidas y modificadas por cualquier función, lo que puede llevar a errores si no se gestionan correctamente.

### Tipos básicos de variables: enteras, flotantes, entre otras

- **Enteras**: `int`, `short`, `long`, `unsigned int`
- **Flotantes**: `float`, `double`
- **Caracteres**: `char`
- **Otros**: `bool` (con la librería `stdbool.h`)

### Identificadores de los diferentes tipos de variable en `printf`

- `%d`: Entero decimal
- `%f`: Flotante
- `%c`: Carácter
- `%s`: Cadena de caracteres
- `%u`: Entero sin signo
- `%x`: Entero hexadecimal

### ¿Qué es el `main`?

La función `main` es el punto de entrada de cualquier programa en C. Es donde comienza la ejecución del programa. Su prototipo común es:
```c
int main(void)
{
    // Código
    return 0;
}
```

### ¿Cómo saber si podremos hacer un programa sin el `main` en C básico?

En C, no es posible crear un programa ejecutable sin la función `main`, ya que es el punto de inicio obligatorio para la ejecución del código.

### ¿Qué es `printf`?

`printf` es una función de la librería estándar `stdio.h` que se utiliza para imprimir texto en la consola. Permite formatear y mostrar diferentes tipos de datos.

### Ejemplo de `printf` imprimiendo varios mensajes

```c
#include <stdio.h>

int main() {
    int numero = 9;
    printf("Hola\n");
    printf("Hola Mundo\n");
    printf("Hola %d Mundo\n", numero);
    printf("%d Hola\n", numero);
    printf("Hola %d\n", numero);
    return 0;
}
```

### Hacer un `printf` que salgan 4 nombres

```c
#include <stdio.h>

int main() {
    printf("Alice\nBob\nCharlie\nDavid\n");
    return 0;
}
```

### ¿Cómo funciona el `scanf`? Traer dos ejemplos

`scanf` se utiliza para leer la entrada del usuario desde la consola. Utiliza especificadores de formato para determinar el tipo de dato a leer.

Ejemplo 1:
```c
#include <stdio.h>

int main() {
    int numero;
    printf("Introduce un numero: ");
    scanf("%d", &numero);
    printf("El numero es: %d\n", numero);
    return 0;
}
```

Ejemplo 2:
```c
#include <stdio.h>

int main() {
    char nombre[50];
    printf("Introduce tu nombre: ");
    scanf("%s", nombre);
    printf("Hola, %s\n", nombre);
    return 0;
}
```

### ¿Qué son los operadores lógicos? Traer un ejemplo de cada uno

Los operadores lógicos en C se utilizan para realizar operaciones lógicas:
- **AND lógico (`&&`)**: Verdadero si ambos operandos son verdaderos.
- **OR lógico (`||`)**: Verdadero si al menos uno de los operandos es verdadero.
- **NOT lógico (`!`)**: Invierte el valor lógico del operando.

Ejemplo:
```c
#include <stdio.h>

int main() {
    int a = 1, b = 0;
    printf("a && b: %d\n", a && b); // 0
    printf("a || b: %d\n", a || b); // 1
    printf("!a: %d\n", !a);         // 0
    return 0;
}
```

### Ejemplo de operadores aritméticos y su existencia en C

Operadores aritméticos básicos en C incluyen:
- **Suma (`+`)**
- **Resta (`-`)**
- **Multiplicación (`*`)**
- **División (`/`)**
- **Módulo (`%`)**

Ejemplo:
```c
#include <stdio.h>

int main() {
    int a = 10, b = 3;
    printf("Suma: %d\n", a + b);
    printf("Resta: %d\n", a - b);
    printf("Multiplicacion: %d\n", a * b);
    printf("Division: %d\n", a / b);
    printf("Modulo: %d\n", a % b);
    return 0;
}
```

### ¿Qué son operadores relacionales? Traer ejemplos

Los operadores relacionales comparan dos valores:
- **Igual a (`==`)**
- **Diferente de (`!=`)**
- **Mayor que (`>`)**
- **Menor que (`<`)**
- **Mayor o igual que (`>=`)**
- **Menor o igual que (`<=`)**

Ejemplo:
```c
#include <stdio.h>

int main() {
    int a = 5, b = 10;
    printf("a == b: %d\n", a == b); // 0
    printf("a != b: %d\n", a != b); // 1
    printf("a > b: %d\n", a > b);   // 0
    printf("a < b: %d\n", a < b);   // 1
    printf("a >= b: %d\n", a >= b); // 0
    printf("a <= b: %d\n", a <= b); // 1
    return 0;
}
```

### Condicional `if`: Ejemplo con una condición y otro con condición verdadera o falsa

Ejemplo con una condición:
```c
#include <stdio.h>

int main() {
    int numero = 5;
    if (numero > 0) {
        printf("El numero es positivo\n");
    }
    return 0;
}
```

Ejemplo con condición verdadera o falsa:
```c
#include <stdio.h>

int main() {
    int numero = -3;
    if (numero > 0) {
        printf("El numero es positivo\n");
    } else {
        printf("El numero es negativo o cero\n");
    }
    return 0;
}
```

### ¿Qué son condicionales anidados? Ejemplo de `if` anidados

Condicionales anidados son estructuras `if` dentro de otros `if`.

Ejemplo:
```c
#include <stdio.h>

int main() {
    int a = 5, b = 10;
    if (a > 0) {
        if (b > 0) {
            printf("Ambos numeros son positivos\n");
        }
    }
    return 0;


}
```

### ¿Qué son ciclos? Ejemplo del ciclo `for`

Los ciclos permiten repetir un bloque de código múltiples veces. El ciclo `for` es un ciclo con una inicialización, una condición y una actualización.

Ejemplo:
```c
#include <stdio.h>

int main() {
    for (int i = 0; i < 5; i++) {
        printf("Iteracion %d\n", i);
    }
    return 0;
}
```