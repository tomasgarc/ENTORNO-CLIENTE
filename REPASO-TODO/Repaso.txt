# Teoría básica de JavaScript

## 1. Funciones flecha (Arrow Functions)

Las **funciones flecha** son una forma moderna y más corta de escribir funciones en JavaScript. Fueron introducidas en ES6.

### Características principales

* Sintaxis más corta
* No tienen su propio `this` (heredan el `this` del contexto exterior)
* No tienen `arguments`
* No se pueden usar como constructores (`new`)

### Sintaxis

```js
const suma = (a, b) => {
  return a + b;
};
```

Si la función tiene una sola expresión:

```js
const suma = (a, b) => a + b;
```

Con un solo parámetro:

```js
const cuadrado = x => x * x;
```

Sin parámetros:

```js
const saludar = () => "Hola";
```

---

## 2. Funciones anónimas

Las **funciones anónimas** son funciones que **no tienen nombre**. Normalmente se usan como valores o callbacks.

### Sintaxis

```js
const suma = function (a, b) {
  return a + b;
};
```

### Usos comunes

* Callbacks
* Eventos
* Temporizadores

Ejemplo:

```js
setTimeout(function () {
  console.log("Hola");
}, 1000);
```

### Características

* Tienen su propio `this`
* No se reutilizan fácilmente
* Son útiles para código puntual

---

## 3. Funciones recursivas

Una **función recursiva** es una función que **se llama a sí misma**.

### Reglas básicas

* Debe tener un **caso base** para evitar bucles infinitos
* Debe acercarse al caso base en cada llamada

### Ejemplo

```js
function factorial(n) {
  if (n === 0) {
    return 1;
  }
  return n * factorial(n - 1);
}
```

### Usos comunes

* Factoriales
* Potencias
* Recorrido de estructuras

---

## 4. Sintaxis para realizar cambios en el DOM

El **DOM (Document Object Model)** representa la estructura HTML como objetos que JavaScript puede manipular.

### Acceder a elementos

```js
document.getElementById("miId");
document.querySelector("p");
document.querySelectorAll(".clase");
```

### Cambiar contenido

```js
element.textContent = "Nuevo texto";
element.innerHTML = "<b>Texto</b>";
```

### Cambiar atributos

```js
element.value = "Hola";
element.src = "imagen.png";
```

### Cambiar estilos

```js
element.style.color = "red";
```

### Eventos

```js
element.onclick = function () {
  alert("Click");
};
```

---

## 5. Objetos predefinidos de JavaScript

### 5.1 Array

Los **arrays** permiten almacenar varios valores.

```js
let numeros = [1, 2, 3];
```

Métodos comunes:

```js
numeros.push(4);
numeros.pop();
numeros.length;
numeros.sort();
numeros.map(n => n * 2);
```

---

### 5.2 Date

El objeto **Date** se usa para trabajar con fechas y horas.

```js
const hoy = new Date();
hoy.getFullYear();
hoy.getMonth();
hoy.getDate();
```

---

### 5.3 Math

El objeto **Math** contiene funciones matemáticas.

```js
Math.round(4.7);
Math.floor(4.7);
Math.ceil(4.1);
Math.random();
Math.max(1, 5, 10);
```

---

### 5.4 Window

El objeto **window** representa la ventana del navegador.

```js
window.alert("Hola");
window.prompt("Introduce un valor");
window.confirm("¿Seguro?");
```

También incluye:

* `setTimeout()`
* `setInterval()`

---

## 📌 Conclusión

Estos conceptos son la base de JavaScript:

* Las funciones permiten organizar el código
* El DOM permite interactuar con la página
* Los objetos predefinidos facilitan tareas comunes

Dominar esto te permite crear aplicaciones web dinámica