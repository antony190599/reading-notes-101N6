# **Tipos de Objetos**

### **1. ¿Cuál es la diferencia entre un string primitivo y un objeto String en JavaScript? ¿En qué situaciones conviene usar cada uno?**  
- **String primitivo:**
  
  Es un valor inmutable que representa texto. Se utiliza en la mayoría de los casos por ser más ligero y eficiente.  
  ```
  const texto = "Hola, mundo"; // String primitivo
  ```
- **Objeto String:**

  Es un envoltorio (wrapper) que ofrece métodos adicionales para manipular cadenas.
  ```
  const textoObjeto = new String("Hola, mundo"); // Objeto String
  ```
💡 Usar primitivos para operaciones comunes; usar objetos String solo si necesitas propiedades adicionales o tratar un string como un objeto.

### **2. Explica cómo funcionan y en qué casos utilizarías los métodos substring(), slice() y split() del objeto String.**

**substring(start, end)**

  Devuelve una subcadena desde start hasta end (no incluye el índice end).
```
  "Hola, mundo".substring(0, 4); // "Hola"
```
**slice(start, end)**
  
  Similar a substring(), pero admite índices negativos para contar desde el final.
```
  "Hola, mundo".slice(-5, -1); // "mund"
```
  **split(separator)**
  Divide la cadena en un arreglo con base en un separador.
```
  "Hola, mundo".split(", "); // ["Hola", "mundo"]
```
💡 Uso:

- **substring()** y **slice()** para extraer partes de una cadena.

- **split()** para transformar cadenas en arreglos.
### **3. ¿Qué diferencia existe entre los métodos push(), pop(), shift() y unshift() del objeto Array? Proporciona ejemplos de uso.**

- **push():** Agrega un elemento al final del arreglo.
```
const numeros = [1, 2];
numeros.push(3); // [1, 2, 3]
```
- **pop():** Elimina y devuelve el último elemento.
```
numeros.pop(); // [1, 2], devuelve 3
```
- **shift():** Elimina y devuelve el primer elemento.
```
numeros.shift(); // [2], devuelve 1
```
- **unshift():** Agrega uno o más elementos al inicio del arreglo.
```
numeros.unshift(0); // [0, 2]
```
💡 Usar según la posición donde necesites agregar o quitar elementos.

### **4. ¿Cómo utilizarías los métodos de Array para transformar y filtrar datos en una colección? Da un ejemplo práctico utilizando map(), filter() o reduce().**

**Ejemplo práctico:**

Supongamos que tenemos una lista de números y queremos:

- Multiplicar cada número por 2.
- Filtrar los números mayores a 10.
- Sumar los números restantes.
```
const numeros = [3, 5, 7, 10];

const transformados = numeros
  .map(num => num * 2)            // [6, 10, 14, 20]
  .filter(num => num > 10)        // [14, 20]
  .reduce((acum, num) => acum + num, 0); // 34

console.log(transformados); // 34
```
💡 Ventaja: Usar métodos funcionales como map(), filter() y reduce() hace que el código sea más declarativo y fácil de entender.

### **5. Fuentes y Recursos Adicionales**

[Aprende más sobre el objeto String](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/String)

[Explora los métodos de Array](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array)

### **6. Cosas que quiero saber más**

💡 Pregunta:

¿Cómo optimizar el uso de métodos de Array en grandes volúmenes de datos sin afectar el rendimiento?
