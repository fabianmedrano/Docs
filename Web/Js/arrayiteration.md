
1. **forEach()**: Esta función ejecuta una función proporcionada una vez para cada elemento del array.
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   arr.forEach(function(element) {
       console.log(element);
   });
   ```
2. **map()**: Esta función crea un nuevo array con los resultados de la llamada a una función proporcionada en cada elemento del array.
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   let newArr = arr.map(function(element) {
       return element * 2;
   });
   console.log(newArr); // [2, 4, 6, 8, 10]
   ```
3. **filter()**: Esta función crea un nuevo array con todos los elementos que pasen una prueba (la función proporcionada).
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   let newArr = arr.filter(function(element) {
       return element % 2 === 0;
   });
   console.log(newArr); // [2, 4]
   ```
4. **reduce()**: Esta función aplica una función a un acumulador y a cada valor de un array (de izquierda a derecha) para reducirlo a un solo valor.
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   let sum = arr.reduce(function(total, element) {
       return total + element;
   }, 0);
   console.log(sum); // 15
   ```
5. **some()**: Esta función verifica si al menos un elemento del array cumple con la prueba implementada por la función proporcionada.
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   let hasEvenNumber = arr.some(function(element) {
       return element % 2 === 0;
   });
   console.log(hasEvenNumber); // true
   ```
6. **every()**: Esta función verifica si todos los elementos del array cumplen con la prueba implementada por la función proporcionada.
   ```javascript
   let arr = [1, 2, 3, 4, 5];
   let allAreEvenNumbers = arr.every(function(element) {
       return element % 2 === 0;
   });
   console.log(allAreEvenNumbers); // false
   ```
