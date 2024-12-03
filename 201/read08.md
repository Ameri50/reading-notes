<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Strings y Arrays en JavaScript</title>
</head>
<body>
  <h1>Strings y Arrays en JavaScript</h1>

  <h2>String primitivo vs Objeto String</h2>
  <p><strong>String primitivo:</strong> Es un valor simple de tipo <code>string</code>, más ligero y eficiente para la mayoría de los casos.</p>
  <p><strong>Objeto String:</strong> Es una instancia del constructor <code>String</code>, más pesado pero útil si necesitas métodos adicionales o tratar el string como un objeto.</p>
  <p><strong>Ejemplo:</strong></p>
  <pre><code>// String primitivo
let primitivo = "Hola";

// Objeto String
let objetoString = new String("Hola");

console.log(typeof primitivo); // "string"
console.log(typeof objetoString); // "object"</code></pre>
  <p><strong>¿Cuándo usar cada uno?</strong> Usa strings primitivos por defecto, ya que son más rápidos. Utiliza el objeto <code>String</code> solo si necesitas métodos adicionales del prototipo de String.</p>

  <h2>Métodos substring(), slice() y split()</h2>
  <ul>
    <li><strong>substring(start, end):</strong> Extrae una parte de la cadena entre dos índices (sin incluir el índice final).
      <pre><code>let str = "JavaScript";
console.log(str.substring(0, 4)); // "Java"</code></pre>
    </li>
    <li><strong>slice(start, end):</strong> Similar a <code>substring()</code>, pero permite índices negativos para contar desde el final.
      <pre><code>console.log(str.slice(-6, -1)); // "Scrip"</code></pre>
    </li>
    <li><strong>split(separator):</strong> Divide la cadena en un arreglo según un separador.
      <pre><code>let words = "a,b,c".split(","); 
console.log(words); // ["a", "b", "c"]</code></pre>
    </li>
  </ul>

  <h2>Métodos push(), pop(), shift() y unshift() en Arrays</h2>
  <ul>
    <li><strong>push():</strong> Agrega elementos al final del arreglo.
      <pre><code>let arr = [1, 2];
arr.push(3);
console.log(arr); // [1, 2, 3]</code></pre>
    </li>
    <li><strong>pop():</strong> Elimina y devuelve el último elemento.
      <pre><code>arr.pop();
console.log(arr); // [1, 2]</code></pre>
    </li>
    <li><strong>shift():</strong> Elimina y devuelve el primer elemento.
      <pre><code>arr.shift();
console.log(arr); // [2]</code></pre>
    </li>
    <li><strong>unshift():</strong> Agrega elementos al inicio del arreglo.
      <pre><code>arr.unshift(0);
console.log(arr); // [0, 2]</code></pre>
    </li>
  </ul>

  <h2>Transformar y filtrar datos en un arreglo</h2>
  <p>Podemos usar métodos como <code>map()</code>, <code>filter()</code> y <code>reduce()</code> para manipular arreglos de forma declarativa.</p>
  <p><strong>Ejemplo práctico:</strong></p>
  <pre><code>// Lista de números
let nums = [1, 2, 3, 4, 5];

// Duplicar números pares
let paresDuplicados = nums
  .filter(x => x % 2 === 0)    // Filtra números pares
  .map(x => x * 2);            // Duplica los números

console.log(paresDuplicados); // [4, 8]

// Sumar todos los números
let suma = nums.reduce((acc, x) => acc + x, 0);
console.log(suma); // 15</code></pre>
</body>
</html>
