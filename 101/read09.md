### 1. **Tipos de Datos en JavaScript**
En JavaScript, existen dos categorías principales de tipos de datos:

- **Primitivos**:
  - `number`: Representa valores numéricos, enteros o decimales.
  - `string`: Cadenas de texto.
  - `boolean`: Valores de verdadero (`true`) o falso (`false`).
  - `undefined`: Sin valor asignado.
  - `null`: Representa un valor vacío.
  - `symbol`: Valor único e inmutable.
  - `bigint`: Enteros de gran tamaño.

- **Objetos**:
  - Pueden contener múltiples valores y tipos complejos (como *arrays*, *objetos personalizados*) y se pueden modificar.

---

### 2. **Estructuras Condicionales: `if` y `else`**
Las estructuras condicionales se usan para controlar el flujo de un programa, ejecutando bloques específicos de código según ciertas condiciones.

```
if (condition) {
  // Código a ejecutar si la condición es verdadera
} else {
  // Código a ejecutar si la condición es falsa
}
```

- if: Evalúa una condición y ejecuta el bloque asociado si es verdadera.

- else: Define un bloque alternativo para ejecutar si la condición del if es falsa.

**3. Operadores en JavaScript**

Existen diferentes tipos de operadores:

Aritméticos: Realizan cálculos matemáticos.
```
let suma = 5 + 3;      // 8

let resta = 10 - 4;    // 6

let producto = 2 * 3;  // 6

let division = 10 / 2; // 5

let modulo = 10 % 3;   // 1
```

- Comparación: ==, ===, !=, !==, >, <, >=, <=

- Lógicos: &&, ||, !

- Asignación: =, +=, -=, *=, /=

- Ternario: Condicional en una sola línea: condition ? expr1 : expr2

**4. Declaración de Variables**

En JavaScript, las variables se declaran con var, let o const, cada una con sus características de alcance y mutabilidad:

- var:

Permite re-declaración y modificación dentro de la misma función.

- let:

Permite modificación, pero no re-declaración en el mismo bloque.

- const:

No permite re-declaración ni modificación del valor asignado.

```
var nombre = "Ana";  // Se puede re-declarar y modificar

let edad = 25;       // Se puede modificar, pero no re-declarar en el mismo bloque

const ciudad = "Lima"; // No se puede modificar ni re-declarar
```
