# **Funciones y Callbacks en JavaScript**

### **1. ¿Cuáles son las diferentes formas de declarar una función en JavaScript? Explica las diferencias entre una declaración de función, una expresión de función y una función flecha.**  

- **Declaración de función:**  

  Una forma clásica y completa de declarar una función. Es elevada (hoisted), lo que significa que puedes usarla antes de declararla en el código.  
  ```
  function sumar(a, b) {
    return a + b;
  }
  console.log(sumar(2, 3)); // 5
  ```
- **Expresión de función:**

  Asigna una función a una variable. No se eleva, por lo que debes declararla antes de usarla.
  ```
  const restar = function (a, b) {
    return a - b;
  };
  console.log(restar(5, 2)); // 3
  ```
- **Función flecha:**

  Introducida en ES6, es una forma más concisa de escribir funciones. No tiene su propio contexto de this.
  ```
  const multiplicar = (a, b) => a * b;
  console.log(multiplicar(4, 3)); // 12
  ```
  💡 Diferencia clave: La declaración de función se eleva, mientras que las expresiones y funciones flecha no.

### **2. ¿Qué es una función callback y por qué son importantes en JavaScript? Proporciona un ejemplo práctico de su uso.**
  
  Una función callback es una función pasada como argumento a otra función, que se ejecuta después de que se completa una operación. Son esenciales para manejar operaciones asincrónicas, como el manejo de eventos o llamadas a APIs.

  Ejemplo práctico:
  ```
  function procesarUsuario(nombre, callback) {
    console.log(`Hola, ${nombre}`);
    callback();
  }

  function despedida() {
    console.log("Adiós, nos vemos pronto.");
  }

  procesarUsuario("Ana", despedida);
  // Salida:
  // Hola, Ana
  // Adiós, nos vemos pronto.
  ```
  💡 Importancia: Facilitan la ejecución secuencial o condicional de código, especialmente en operaciones asincrónicas.

### **3. ¿Cómo afecta el hoisting a las declaraciones de funciones? ¿Existe alguna diferencia en cómo se manejan las funciones declaradas versus las expresiones de función?**

  **Declaraciones de funciones:**

  Son elevadas (hoisted), lo que significa que pueden usarse antes de ser declaradas.
  ```
  saludar();
  function saludar() {
    console.log("Hola!");
  }
  // Salida: Hola!
  ```
  **Expresiones de función y funciones flecha:**
  
  No se elevan. Si intentas usarlas antes de declararlas, obtendrás un error.
  ```
  intentar();
  const intentar = function () {
    console.log("Esto no funcionará.");
  };
  // Error: intentar no es una función
  ```

💡 Diferencia clave: Las declaraciones de funciones son accesibles antes de su definición, mientras que las expresiones de función y funciones flecha no lo son.

### **4. Fuentes y Recursos Adicionales**

[Aprende más sobre funciones en JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Functions)

[Descubre más sobre callbacks y programación asincrónica](https://developer.mozilla.org/es/docs/Glossary/Callback_function)


### **5. Cosas que quiero saber más**

💡 Pregunta:

¿Cómo se pueden evitar los problemas de callback hell utilizando funciones como Promise o async/await?








