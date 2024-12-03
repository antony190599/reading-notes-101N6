# **Paradigmas de la Programación 1**

### **1. ¿Qué es la programación funcional y cuáles son sus principales características que la diferencian de otros paradigmas de programación?**  
La programación funcional es un paradigma que se basa en funciones puras y evita modificar el estado global. Sus principales características son:  
- **Funciones puras:** No tienen efectos secundarios y siempre producen el mismo resultado para las mismas entradas.  
- **Inmutabilidad:** Los datos no se modifican directamente; en su lugar, se crean copias.  
- **Composición de funciones:** Se combinan funciones más pequeñas para resolver problemas complejos.  
- **Declarativa:** Describe qué se quiere lograr en lugar de cómo hacerlo.  

---

### **2. ¿Cómo aplicarías el principio DRY en un proyecto de JavaScript? Proporciona un ejemplo práctico de código antes y después de aplicar este principio.**  
El principio **DRY** ("Don't Repeat Yourself") evita la duplicación de código.  

- **Antes (código repetido):**  
  ```
  function calcularAreaRectangulo(largo, ancho) {
    return largo * ancho;
  }

  function calcularAreaCuadrado(lado) {
    return lado * lado;
  }


- **Después (código optimizado):**
```
function calcularArea(figura, dimension1, dimension2 = dimension1) {
  return figura === "rectangulo" ? dimension1 * dimension2 : dimension1 * dimension1;
}
```

💡 Ventaja: Centralizar la lógica reduce errores y facilita el mantenimiento.

## **3. ¿Cuáles son las ventajas de utilizar métodos funcionales como map(), filter() y reduce() en lugar de bucles tradicionales?**

- **map():** Transforma cada elemento de un arreglo sin modificar el original.

Ideal para crear un nuevo arreglo a partir de los valores originales.

- **filter():** Selecciona elementos según una condición específica.

Perfecto para crear subarreglos.

- **reduce():** Acumula valores en una sola salida.

Útil para sumar, concatenar o calcular resultados complejos.

💡 Ventajas comunes:

- Código más legible y declarativo.
- Evita mutaciones accidentales en el arreglo original.
## **4. ¿De qué manera el principio DRY y la programación funcional se complementan entre sí para escribir código más mantenible y escalable?**
- La programación funcional fomenta la reutilización de funciones puras, lo que alinea con el principio DRY.
- Evita la duplicación de lógica mediante métodos como map(), filter() y reduce() resulta en código modular y fácil de mantener.
- Juntos, promueven un desarrollo limpio, donde cada pieza de código tiene una única responsabilidad.
## **5. Fuentes y Recursos Adicionales**

Aprende más sobre programación funcional:

[Programación funcional en JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Functional_programming)

Explora el principio DRY:

[DRY: Mejores prácticas en desarrollo](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)

## **6. Cosas que quiero saber más**
   
💡 Pregunta:

¿Cómo adaptar paradigmas funcionales en proyectos que combinan patrones de programación orientada a objetos y funcional?
