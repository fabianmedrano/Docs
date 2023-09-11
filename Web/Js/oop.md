6. **Programación Orientada a Objetos (POO)**:

   ```javascript
   // Clase y objetos
   class Persona {
     constructor(nombre, edad) {
       this.nombre = nombre;
       this.edad = edad;
     }

     saludar() {
       console.log(`Hola, soy ${this.nombre} y tengo ${this.edad} años.`);
     }
   }

   const persona1 = new Persona('Juan', 30);
   const persona2 = new Persona('María', 25);

   persona1.saludar(); // Salida: 'Hola, soy Juan y tengo 30 años.'
   persona2.saludar(); // Salida: 'Hola, soy María y tengo 25 años.'
   ```