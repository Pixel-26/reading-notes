# Read 9: Introducción a Javascript

## 1. ¿Cuáles son los diferentes tipos de datos que se pueden utilizar en JavaScript y cómo se diferencian entre sí?

JavaScript maneja varios tipos de datos, que se dividen en dos categorías principales: **primitivos** y **objetos**.

### 1. Tipos de Datos Primitivos

Los tipos primitivos son valores inmutables. Son los siguientes:

- **Boolean**: Representa un valor lógico. Puede ser `true` (verdadero) o `false` (falso).
- **Null**: Representa la ausencia intencional de cualquier valor o objeto. Se usa para indicar que una variable no tiene valor.
- **Undefined**: Indica que una variable ha sido declarada pero no ha recibido un valor asignado.
- **Number**: Representa valores numéricos, tanto enteros como decimales (flotantes).
- **BigInt**: Es un tipo de dato numérico que permite representar valores enteros muy grandes, fuera del rango del tipo `Number`.
- **String**: Representa una cadena de caracteres, es decir, texto.
- **Symbol**: Representa un valor único e inmutable que puede ser útil para la creación de identificadores u objetos únicos.

### 2. Objetos

Los objetos en JavaScript son estructuras de datos que contienen propiedades y métodos. Son más complejos que los tipos primitivos y pueden almacenar colecciones de datos, como matrices o funciones.

---

## 2. ¿Cómo se utilizan las estructuras condicionales if y else en JavaScript, y qué propósito cumplen dentro de un programa?

Las estructuras condicionales permiten tomar decisiones dentro de un programa basadas en si una condición es verdadera o falsa.

- **`if`**: Evalúa una condición. Si la condición es verdadera (`true`), ejecuta el bloque de código dentro de las llaves `{}`.
  
  ```javascript
  if (condición) {
    // Código a ejecutar si la condición es verdadera
  }
  ```

- **`else`**: Se ejecuta cuando la condición del `if` es falsa (`false`). Permite definir una acción alternativa.

  ```javascript
  if (condición) {
    // Código a ejecutar si la condición es verdadera
  } else {
    // Código a ejecutar si la condición es falsa
  }
  ```

Estas estructuras permiten que el programa siga diferentes caminos, dependiendo de las condiciones que se verifiquen.

---

## 3. ¿Cuáles son los diferentes tipos de operadores en JavaScript y cómo se utilizan los operadores aritméticos para realizar cálculos?

JavaScript tiene varios tipos de operadores. A continuación, se describen los más comunes.

### 1. Operadores Aritméticos

Los operadores aritméticos se utilizan para realizar cálculos matemáticos:

- `+` : Suma.
- `-` : Resta.
- `*` : Multiplicación.
- `/` : División.
- `%` : Módulo (resto de una división).
- `++` : Incremento (aumenta el valor de la variable en 1).
- `--` : Decremento (disminuye el valor de la variable en 1).

**Ejemplo:**

```javascript
let a = 10;
let b = 5;
console.log(a + b);  // Suma, resultado: 15
```

### 2. Operadores de Asignación

Los operadores de asignación se utilizan para asignar valores a las variables:

- `=` : Asigna un valor.
- `+=` : Suma y asigna.
- `-=` : Resta y asigna.
- `*=` : Multiplica y asigna.
- `/=` : Divide y asigna.
- `%=` : Módulo y asigna.

**Ejemplo:**

```javascript
let x = 10;
x += 5;  // Equivalente a x = x + 5, ahora x = 15
```

### 3. Operadores de Comparación

Los operadores de comparación se utilizan para comparar valores:

- `==` : Igualdad (no tiene en cuenta el tipo de dato).
- `===` : Igualdad estricta (compara tanto el valor como el tipo de dato).
- `!=` : Desigualdad (no tiene en cuenta el tipo de dato).
- `!==` : Desigualdad estricta (compara tanto el valor como el tipo de dato).
- `>` : Mayor que.
- `<` : Menor que.
- `>=` : Mayor o igual que.
- `<=` : Menor o igual que.

**Ejemplo:**

```javascript
let a = 10;
let b = "10";
console.log(a == b);   // true (compara solo el valor)
console.log(a === b);  // false (compara valor y tipo)
```

### 4. Operadores Lógicos

Los operadores lógicos permiten combinar varias condiciones:

- `&&` : Y lógico (solo es verdadero si ambas condiciones son verdaderas).
- `||` : O lógico (es verdadero si al menos una condición es verdadera).
- `!`  : No lógico (invierte el valor de la condición).

**Ejemplo:**

```javascript
let a = true;
let b = false;
console.log(a && b);   // false
console.log(a || b);   // true
console.log(!a);       // false
```

### 5. Operadores Bit a Bit

Estos operadores operan con la representación binaria de los números:

- `&` : AND bit a bit.
- `|` : OR bit a bit.
- `~` : NOT bit a bit.
- `^` : XOR bit a bit.
- `<<` : Desplazamiento a la izquierda.
- `>>` : Desplazamiento a la derecha.
- `>>>` : Desplazamiento a la derecha sin signo.

**Ejemplo:**

```javascript
let a = 5;  // 0101 en binario
let b = 3;  // 0011 en binario
console.log(a & b);  // Resultado: 1 (0001 en binario)
```

### 6. Operadores de Cadena

- `+` : Se usa para concatenar cadenas de texto.

**Ejemplo:**

```javascript
let nombre = "Juan";
let saludo = "Hola " + nombre;  // "Hola Juan"
```

### 7. Operador Condicional (Ternario)

El operador ternario es una forma compacta de escribir una estructura `if-else`.

**Sintaxis:**

```javascript
condición ? valor_si_verdadero : valor_si_falso;
```

**Ejemplo:**

```javascript
let edad = 18;
let esMayor = (edad >= 18) ? "Mayor de edad" : "Menor de edad";
console.log(esMayor);  // "Mayor de edad"
```

---

## 4. ¿Cómo se declara una variable en JavaScript y cuáles son las diferencias entre var, let y const en cuanto a su alcance y mutabilidad?

En JavaScript, las variables se pueden declarar usando las palabras clave `var`, `let` o `const`.

### 1. **`var`**

- **Alcance**: Función o global.
- **Mutabilidad**: Puede ser redeclarada y reasignada.
- **Hoisting**: Las declaraciones se "elevan" al principio del alcance, lo que significa que la variable puede ser utilizada antes de ser declarada.

```javascript
var x = 10;
```

### 2. **`let`**

- **Alcance**: Bloque (dentro de `{}`).
- **Mutabilidad**: Puede ser reasignada, pero no redeclarada en el mismo alcance.
- **Hoisting**: No tiene el mismo comportamiento de hoisting que `var`.

```javascript
let y = 20;
```

### 3. **`const`**

- **Alcance**: Bloque (dentro de `{}`).
- **Mutabilidad**: No puede ser redeclarada ni reasignada. Es utilizada para declarar constantes.
- **Hoisting**: Similar a `let`, pero su valor no puede cambiar.

```javascript
const z = 30;
```

