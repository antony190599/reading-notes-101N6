# **Prototipos en JavaScript**

### **1. ¿Qué es un prototipo en JavaScript y cómo se relaciona con la herencia? Proporciona un ejemplo de cómo crear una cadena de prototipos.**  
Un **prototipo** es un objeto del que otros objetos pueden heredar propiedades y métodos. En JavaScript, cada objeto tiene un prototipo, lo que permite establecer relaciones de herencia mediante la **cadena de prototipos**.  

- **Ejemplo:**  
  ```javascript
  const animal = {
    comer() {
      console.log("Este animal está comiendo.");
    },
  };

  const perro = Object.create(animal);
  perro.ladrar = function () {
    console.log("El perro está ladrando.");
  };

  perro.comer(); // Este animal está comiendo.
  perro.ladrar(); // El perro está ladrando.

### **2. Cuando hablamos de la relación Modelo/Instancia en JavaScript, ¿qué diferencia existe entre una clase y una instancia de esa clase? ¿Cómo se crean las instancias?**
**Clase:** Es una plantilla que define las propiedades y métodos comunes para sus instancias.

**Instancia:** Es un objeto creado a partir de una clase, con sus propios valores para las propiedades definidas en la clase.

**Ejemplo:**

```
class Animal {
  constructor(nombre) {
    this.nombre = nombre;
  }

  hablar() {
    console.log(`${this.nombre} está haciendo un sonido.`);
  }
}

const perro = new Animal("Fido"); // Instancia de la clase Animal
perro.hablar(); // Fido está haciendo un sonido.
```

💡 Diferencia clave: La clase es el modelo, mientras que la instancia es un objeto específico creado a partir de ese modelo.

### **3. ¿Cómo funciona la herencia de propiedades y métodos en JavaScript? Explica el concepto de la cadena de prototipos con un ejemplo práctico.**

La herencia en JavaScript funciona a través de la cadena de prototipos:

Cuando se accede a una propiedad o método en un objeto, el motor de JavaScript busca primero en ese objeto.

Si no lo encuentra, busca en su prototipo, y así sucesivamente, hasta llegar a Object.prototype o un prototipo null.

**Ejemplo:**
```
function Animal(nombre) {
  this.nombre = nombre;
}
Animal.prototype.hablar = function () {
  console.log(`${this.nombre} hace un sonido.`);
};

function Perro(nombre) {
  Animal.call(this, nombre); // Hereda las propiedades
}
Perro.prototype = Object.create(Animal.prototype); // Hereda métodos
Perro.prototype.constructor = Perro;

const miPerro = new Perro("Rex");
miPerro.hablar(); // Rex hace un sonido.
```

💡 Explicación: miPerro hereda de Perro.prototype, que a su vez hereda de Animal.prototype, formando la cadena de prototipos.

### **4. ¿Cuáles son las mejores prácticas al implementar herencia en JavaScript? ¿Cuándo deberías usar herencia y cuándo podrías considerar otras alternativas?**
Mejores prácticas:

- Usa class para implementar herencia, ya que es más legible y moderno.
- Define métodos comunes en el prototipo para ahorrar memoria.
- Evita cadenas de herencia demasiado profundas, ya que pueden ser difíciles de mantener.
- Cuándo usar herencia:

- Cuando hay una relación clara de "es-un".

**Ejemplo:** Un Perro es un tipo de Animal.

Cuándo considerar alternativas:

Si los objetos tienen comportamientos diferentes pero comparten funcionalidad, considera composición en lugar de herencia.

**Ejemplo:** Usar funciones o mixins para compartir métodos.
```
const volar = {
  volar() {
    console.log("Este objeto puede volar.");
  },
};

const pajaro = Object.assign({}, volar);
pajaro.volar(); // Este objeto puede volar.
```

### **5. Fuentes y Recursos Adicionales**

[Prototipos en JavaScript](https://developer.mozilla.org/es/docs/Learn_web_development/Extensions/Advanced_JavaScript_objects/Object_prototypes)

[Guía de herencia en JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

### **6. Cosas que quiero saber más**

💡 Pregunta:

¿Cuáles son los patrones más comunes para evitar problemas en estructuras complejas de herencia en JavaScript?
