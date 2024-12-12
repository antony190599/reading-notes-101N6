# **Paradigmas de la Programación 2**

### **1. ¿Qué es la abstracción en programación y cómo se implementa utilizando objetos en JavaScript? Proporciona un ejemplo práctico.**  
La **abstracción** oculta los detalles internos de implementación y expone solo las funcionalidades esenciales.  

- **Implementación con objetos:**  
  ```
  class Vehiculo {
    constructor(marca, modelo) {
      this.marca = marca;
      this.modelo = modelo;
    }
    
    obtenerDetalles() {
      return `${this.marca} ${this.modelo}`;
    }
  }

  const auto = new Vehiculo("Toyota", "Corolla");
  console.log(auto.obtenerDetalles()); // Toyota Corolla
  ```
  
💡 Ventaja: Los detalles internos del objeto (como propiedades marca y modelo) están encapsulados, mientras que el método obtenerDetalles() expone la funcionalidad principal.

### **2. ¿Cuáles son los cuatro pilares de la Programación Orientada a Objetos y cómo se aplican en JavaScript?**

- **Abstracción:** Oculta detalles complejos, exponiendo solo lo necesario.
  
   **Ejemplo:** Métodos públicos que interactúan con datos encapsulados.

- **Encapsulación:** Agrupa datos y métodos relacionados en una sola entidad (objeto/clase).

   **Ejemplo:** Usar métodos para modificar propiedades privadas.
  
- **Herencia:** Permite que una clase derive propiedades y métodos de otra.
  
  **Ejemplo:** Una clase Animal de la que heredan Perro y Gato.
  
- **Polimorfismo:** Un método puede tener diferentes implementaciones en clases derivadas.

  **Ejemplo:** Métodos sonido() en Perro y Gato devuelven valores distintos.
  
### **3. ¿Cuál es la diferencia entre un objeto literal y una clase en JavaScript? ¿Cuándo deberías usar cada uno?**

- **Objeto literal:** Declaración rápida y sencilla para una única instancia.

    **Uso:** Datos estáticos o configuraciones.
```
const auto = { marca: "Toyota", modelo: "Corolla" };
```
- **Clase:** Plantilla para crear múltiples instancias con propiedades y métodos compartidos.

     **Uso:** Modelado de estructuras de datos complejas o reutilizables.
```
class Vehiculo {
  constructor(marca, modelo) {
    this.marca = marca;
    this.modelo = modelo;
  }
}
const auto = new Vehiculo("Toyota", "Corolla");
```
### **4. ¿Cómo implementarías la herencia en JavaScript utilizando clases? Proporciona un ejemplo que demuestre la relación padre-hijo entre dos clases.**

**Ejemplo de herencia:**
```
class Animal {
  constructor(nombre) {
    this.nombre = nombre;
  }

  hacerSonido() {
    return `${this.nombre} hace un sonido.`;
  }
}

class Perro extends Animal {
  hacerSonido() {
    return `${this.nombre} ladra.`;
  }
}

const miPerro = new Perro("Fido");
console.log(miPerro.hacerSonido()); // Fido ladra.
```

💡 Relación padre-hijo: La clase Perro hereda de Animal, pero sobrescribe el método hacerSonido().

### **5. Fuentes y Recursos Adicionales**
   
[Aprende sobre POO en JavaScript:](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Classes)

[Conoce más sobre abstracción y herencia:](https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260)


### **6. Cosas que quiero saber más**
💡 Pregunta:

¿Cómo implementar polimorfismo y patrones de diseño avanzados en proyectos grandes usando JavaScript?

¡Domina los paradigmas de la programación orientada a objetos para escribir código robusto y escalable! 🚀





