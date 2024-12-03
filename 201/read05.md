# **Estructuras de Control y Datos en JavaScript**

### **1. ¿Cuáles son los diferentes tipos de estructuras condicionales en JavaScript y en qué situaciones deberías usar cada una?**  
- **`if...else`:** Para ejecutar bloques de código basados en una condición específica.  
  - Ideal para decisiones simples o pocos casos.  
- **`switch`:** Maneja múltiples condiciones basadas en un solo valor.  
  - Útil para reemplazar múltiples `if...else` con condiciones relacionadas.  
- **Operador ternario (`? :`):** Alternativa corta a `if...else`.  
  - Perfecto para condiciones simples que devuelven valores.  

---

### **2. En el contexto de arreglos en JavaScript, ¿cuál es la diferencia entre los métodos `push()`, `unshift()` y `splice()`, y cuándo usarías cada uno?**  
- **`push()`:** Agrega elementos al final del arreglo.  
  - Útil para expandir el arreglo por la parte final.  
- **`unshift()`:** Agrega elementos al inicio del arreglo.  
  - Ideal para insertar datos en la parte frontal.  
- **`splice()`:** Permite agregar, eliminar o reemplazar elementos en posiciones específicas.  
  - Versátil para modificar arreglos en ubicaciones específicas.  

---

### **3. ¿Qué diferencias existen entre los bucles `for`, `while` y `do...while`? Proporciona un ejemplo práctico de uso para cada uno.**  
- **`for`:** Recorre un bloque de código un número definido de veces.  
  - Ejemplo:  
    ```
    for (let i = 0; i < 5; i++) {
      console.log(i);
    }
    ```  
- **`while`:** Ejecuta un bloque de código mientras la condición sea verdadera.  
  - Ejemplo:  
    ```
    let i = 0;
    while (i < 5) {
      console.log(i);
      i++;
    }
    ```  
- **`do...while`:** Similar a `while`, pero asegura que el código se ejecute al menos una vez.  
  - Ejemplo:  
    ```
    let i = 0;
    do {
      console.log(i);
      i++;
    } while (i < 5);
    ```  

---

### **4. ¿Cómo se puede recorrer un arreglo en JavaScript utilizando diferentes tipos de bucles y cuál consideras más eficiente según el caso de uso?**  
- **`for`:** Ideal para iterar con control total sobre índices.  
- **`for...of`:** Simplifica la iteración directamente sobre valores del arreglo.  
  ```
  for (const value of array) {
    console.log(value);
  }
  ```
- **forEach()**: Método de array para ejecutar una función sobre cada elemento.
  
```
array.forEach(value => console.log(value));
```
**while y do...while:** Útiles cuando la iteración depende de condiciones externas.

💡 Elección eficiente: Para arreglos grandes, for o for...of suelen ser más rápidos que forEach() debido a menor overhead.

## **5. Fuentes y Recursos Adicionales**

Aprende más sobre estructuras condicionales:

[Condicionales en JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/if...else)

Explora las opciones para trabajar con bucles:

[Guía de bucles en JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Loops_and_iteration)

## **6. Cosas que quiero saber más**

💡 Pregunta:

¿Cómo optimizar el uso de bucles y métodos de arreglos en JavaScript para mejorar el rendimiento en aplicaciones grandes?


  
