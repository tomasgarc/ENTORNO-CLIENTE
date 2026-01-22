📘 REPASO GENERAL DE JAVASCRIPT

(DOM · Funciones · Sintaxis · Eventos · Objetos predefinidos)

1️⃣ DOM (Document Object Model)

El DOM es la representación del HTML como un árbol de nodos que JavaScript puede manipular.

🔹 Selección de elementos
document.getElementById("id")        // Devuelve un elemento o null
document.querySelector("selector")  // Primer elemento que coincida
document.querySelectorAll("selector") // NodeList
document.getElementsByClassName("clase") // HTMLCollection


👉 querySelectorAll() NO devuelve un array, sino un NodeList
👉 .length devuelve cuántos elementos hay

🔹 Modificar contenido
element.innerHTML   // Modifica HTML
element.textContent // Modifica solo texto

2️⃣ Sintaxis básica de JavaScript
🔹 Variables
let x = 5;      // Variable
const y = 10;   // Constante (no se reasigna)
var z = 3;      // Ámbito global o de función (evitar)


📌 let y const tienen ámbito de bloque

🔹 Condicionales
if (x > 5) {
  console.log("Mayor");
}


❌ No existe then

🔹 Bucles
for (let i = 0; i < 5; i++) {}
while (condicion) {}

3️⃣ Funciones en JavaScript
🔹 Función normal
function suma(a, b) {
  return a + b;
}

🔹 Función anónima
const f = function () {
  console.log("Hola");
};


✔ No tiene nombre
✔ Muy usada en eventos

🔹 Función flecha (arrow function)
const doble = x => x * 2;


✔ Usa =>
✔ Si solo hay una línea, el return es implícito
✔ No crea su propio this

❌ Incorrecto:

x => { x * 2 } // NO devuelve nada

🔹 Función recursiva

Una función que se llama a sí misma.

function factorial(n) {
  if (n === 0) return 1; // condición de salida
  return n * factorial(n - 1);
}


📌 Siempre debe tener condición de salida
❌ Si no → desbordamiento de pila

4️⃣ Eventos

Un evento es una acción del usuario o del navegador.

🔹 Eventos comunes
Evento	Cuándo ocurre
click	Clic del ratón
load	Página cargada
submit	Envío de formulario
mouseover	Ratón encima
🔹 Asignar eventos
element.addEventListener("click", function () {
  console.log("Click");
});


✔ Se suele pasar función anónima o flecha

🔹 Objeto event
event.preventDefault(); // Evita acción por defecto


Ejemplo: evitar envío de formulario

🔹 Eliminar eventos
element.removeEventListener("click", funcion);

5️⃣ Objetos predefinidos
🔹 window

Representa la ventana del navegador

window.alert("Hola");

🔹 document

Permite acceder al DOM

document.title = "Nuevo título";

🔹 console

Depuración

console.log("Mensaje");

🔹 Math
Math.random();      // Número entre 0 y 1
Math.floor(4.9);    // 4

🔹 Date
const hoy = new Date();

🔹 Array
let lista = [1, 2, 3];
lista.push(4); // Añade al final


📌 typeof [] devuelve "object"

6️⃣ Tipos de datos importantes
typeof "hola"        // "string"
typeof 5             // "number"
typeof true          // "boolean"
typeof {}            // "object"
typeof function(){}  // "function"
typeof []            // "object"

7️⃣ Strings (texto)
texto.toLowerCase()
texto.toUpperCase()
texto.replace(/\s+/g, "")


✔ \s → espacios
✔ g → global

8️⃣ Cosas CLAVE de examen ⚠️

✔ querySelectorAll() → NodeList
✔ addEventListener("click", función)
✔ Funciones flecha no tienen su propio this
✔ Función sin return devuelve undefined
✔ getElementById() devuelve null si no existe
✔ submit es el evento de formularios