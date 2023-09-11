
# Variables y Ámbitos en JavaScript

Las variables son uno de los conceptos fundamentales en JavaScript, y se utilizan para almacenar y manipular datos durante la ejecución del programa. En JavaScript, se pueden declarar variables utilizando las palabras clave `var`, `let`, o `const`. Además, el ámbito de una variable determina dónde es accesible dentro del código.

## Variables y Declaración

1. **var**: Anteriormente, `var` era la única forma de declarar variables en JavaScript. Sin embargo, tiene un ámbito de función (no respeta el ámbito de bloque) y puede llevar a errores de hoisting (el proceso de mover las declaraciones de variables y funciones al inicio del ámbito).

   ```javascript
   var x = 10;
   var nombre = "Juan";

   function ejemploVar() {
     if (true) {
       var x = 20; // Aquí se modifica la variable x del ámbito exterior
       console.log(x); // Salida: 20
     }
     console.log(x); // Salida: 20
   }

   ejemploVar();
   console.log(x); // Salida: 20
   ```

2. **let**: Con la introducción de ECMAScript 6 (ES6), se agregó la palabra clave `let`, que tiene un ámbito de bloque. Esto soluciona los problemas de ámbito de `var`.

   ```javascript
   let y = 10;
   let nombre = "María";

   function ejemploLet() {
     if (true) {
       let y = 20; // Aquí se crea una nueva variable y dentro del bloque
       console.log(y); // Salida: 20
     }
     console.log(y); // Salida: 10 (no afectado por el bloque)
   }

   ejemploLet();
   console.log(y); // Salida: 10
   ```

3. **const**: `const` también se introdujo en ES6 y se utiliza para declarar constantes. Una vez que se asigna un valor a una constante, no se puede reasignar.

   ```javascript
   const PI = 3.14159;
   const nombre = "Pedro";

   // Intentar reasignar una constante generará un error:
   PI = 3.14; // Esto generará un error
   ```

## Ámbito de las Variables

El ámbito de una variable determina en qué parte del código es accesible y dónde deja de serlo. En JavaScript, hay tres ámbitos principales:

1. **Ámbito global**: Las variables declaradas fuera de cualquier función tienen un ámbito global y son accesibles desde cualquier parte del código.

   ```javascript
   var globalVar = "Soy global";

   function ejemploGlobal() {
     console.log(globalVar); // Salida: "Soy global"
   }

   ejemploGlobal();
   console.log(globalVar); // Salida: "Soy global"
   ```

2. **Ámbito de función**: Las variables declaradas dentro de una función tienen un ámbito local y solo son accesibles dentro de esa función.

   ```javascript
   function ejemploFuncion() {
     var localVar = "Soy local";
     console.log(localVar); // Salida: "Soy local"
   }

   ejemploFuncion();
   // La siguiente línea generará un error, ya que localVar no es accesible fuera de la función:
   console.log(localVar);
   ```

3. **Ámbito de bloque**: Las variables declaradas con `let` o `const` tienen un ámbito de bloque y son accesibles solo dentro del bloque donde se declaran.

   ```javascript
   function ejemploBloque() {
     if (true) {
       let bloqueVar = "Soy de bloque";
       console.log(bloqueVar); // Salida: "Soy de bloque"
     }
     // La siguiente línea generará un error, ya que bloqueVar no es accesible fuera del bloque:
     console.log(bloqueVar);
   }

   ejemploBloque();
   ```

Es importante tener en cuenta el ámbito de las variables para evitar errores y mantener un código claro y organizado. El uso adecuado de `var`, `let`, y `const`, junto con la comprensión de los ámbitos.
