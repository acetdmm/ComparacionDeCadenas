# Comparación de Cadenas en C++

Este programa en C++ permite comparar dos cadenas de caracteres utilizando la función `strcmp()` de la biblioteca `<cstring>`. La comparación determina si las cadenas son iguales, si una es mayor que la otra, o si una es menor.

## Propósito del Código

El objetivo principal del programa es realizar una comparación alfabética entre dos cadenas de caracteres (strings) y mostrar un mensaje en la consola indicando el resultado de la comparación. Este tipo de funcionalidad es útil en aplicaciones donde se necesite ordenar, filtrar o comparar texto, como en bases de datos o sistemas de búsqueda.

## ¿Qué incluye el código?

1. **Declaración de Cadenas**
   - Se definen dos cadenas constantes (`str1` y `str2`):
     ```cpp
     const char* str1 = "arma3";
     const char* str2 = "reddeadredemption2";
     ```

2. **Comparación con `strcmp`**
   - La función `strcmp()` compara las cadenas carácter por carácter y devuelve:
     - `0` si las cadenas son iguales.
     - Un valor negativo si la primera cadena es menor que la segunda.
     - Un valor positivo si la primera cadena es mayor que la segunda.
     ```cpp
     int result = strcmp(str1, str2);
     ```

3. **Condicionales para Interpretar el Resultado**
   - El programa utiliza estructuras condicionales para interpretar el resultado de `strcmp()` y mostrar mensajes correspondientes:
     ```cpp
     if (result == 0) {
         cout << "Las cadenas son iguales." << endl;
     } else if (result < 0) {
         cout << "La cadena \"" << str1 << "\" es menor que \"" << str2 << "\"." << endl;
     } else {
         cout << "La cadena \"" << str1 << "\" es mayor que \"" << str2 << "\"." << endl;
     }
     ```

4. **Salida del Resultado**
   - Para las cadenas `arma3` y `reddeadredemption2`, el programa imprimirá:
     ```plaintext
     La cadena "arma3" es menor que "reddeadredemption2".
     ```

## ¿Cómo usar el programa?

1. **Compilación del Código**
   - Usa un compilador de C++ para compilar el archivo fuente:
     ```bash
     g++ comparacionDeCadenas.cpp -o comparacionDeCadenas
     ```

2. **Ejecución del Programa**
   - Ejecuta el programa desde la terminal:
     ```bash
     ./comparacionDeCadenas
     ```

3. **Resultados**
   - El programa imprimirá si las cadenas son iguales, o cuál de las dos es mayor según el orden alfabético.

## Características Técnicas

- **Comparación Alfabética:** Se utiliza la función `strcmp()` para realizar comparaciones basadas en el código ASCII de los caracteres.
- **Resultados Intuitivos:** El programa muestra mensajes claros y legibles en la consola para interpretar los resultados.
- **Cadenas Constantes:** Las cadenas de caracteres se definen como constantes (`const char*`) para evitar modificaciones accidentales.

## Personalización

Puedes modificar las cadenas de caracteres en el código para realizar comparaciones entre otros textos. Por ejemplo:
```cpp
const char* str1 = "banana";
const char* str2 = "apple";
