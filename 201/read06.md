<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Programación Funcional y Principios en JavaScript</title>
</head>
<body>
  <h1>Programación Funcional y Principios en JavaScript</h1>

  <h2>¿Qué es la programación funcional?</h2>
  <ul>
    <li><strong>Definición:</strong> Un paradigma de programación basado en funciones puras y datos inmutables.</li>
    <li><strong>Características principales:</strong>
      <ul>
        <li><strong>Funciones puras:</strong> No tienen efectos secundarios y su salida depende únicamente de sus entradas.</li>
        <li><strong>Inmutabilidad:</strong> Los datos no se modifican, se crean nuevas estructuras en su lugar.</li>
        <li><strong>Funciones de orden superior:</strong> Pueden recibir y devolver otras funciones.</li>
        <li><strong>Transparencia referencial:</strong> Una función siempre devuelve el mismo resultado dado el mismo input.</li>
      </ul>
    </li>
  </ul>

  <h2>Aplicar el principio DRY (Don't Repeat Yourself) en JavaScript</h2>
  <p><strong>Ejemplo antes de aplicar DRY:</strong></p>
  <pre><code>function calcularAreaCirculo(radio) {
  return Math.PI * radio * radio;
}

function calcularPerimetroCirculo(radio) {
  return 2 * Math.PI * radio;
}</code></pre>

  <p><strong>Ejemplo después de aplicar DRY:</strong></p>
  <pre><code>function calcularCirculo(radio, esArea) {
  return esArea ? Math.PI * radio * radio : 2 * Math.PI * radio;
}

// Uso:
calcularCirculo(5, true);  // Área
calcularCirculo(5, false); // Perímetro</code></pre>

  <h2>Ventajas de métodos funcionales como map(), filter() y reduce()</h2>
  <ul>
    <li><strong>map():</strong> Transforma cada elemento del arreglo y devuelve un nuevo arreglo.
      <pre><code>let nums = [1, 2, 3];
let doubled = nums.map(x => x * 2); // [2, 4, 6]</code></pre>
    </li>
    <li><strong>filter():</strong> Filtra elementos que cumplen con una condición.
      <pre><code>let nums = [1, 2, 3];
let evens = nums.filter(x => x % 2 === 0); // [2]</code></pre>
    </li>
    <li><strong>reduce():</strong> Combina elementos en un solo valor.
      <pre><code>let nums = [1, 2, 3];
let sum = nums.reduce((acc, x) => acc + x, 0); // 6</code></pre>
    </li>
    <li><strong>Ventajas:</strong>
      <ul>
        <li>Son más expresivos y concisos.</li>
        <li>Evitan mutaciones de datos.</li>
        <li>Facilitan la escritura de código declarativo.</li>
      </ul>
    </li>
  </ul>

  <h2>Cómo el principio DRY y la programación funcional se complementan</h2>
  <ul>
    <li><strong>Relación:</strong> Ambos buscan reducir redundancias y escribir código más limpio.</li>
    <li><strong>Beneficios combinados:</strong>
      <ul>
        <li>La programación funcional fomenta reutilizar funciones puras, alineándose con DRY.</li>
        <li>Los métodos funcionales como <code>map()</code>, <code>filter()</code>, y <code>reduce()</code> eliminan la necesidad de escribir bucles repetitivos.</li>
      </ul>
    </li>
    <li><strong>Ejemplo práctico:</strong></li>
    <pre><code>// Código repetitivo:
let sumaDobles = 0;
for (let i = 0; i < nums.length; i++) {
  if (nums[i] % 2 === 0) {
    sumaDobles += nums[i] * 2;
  }
}

// Con DRY y programación funcional:
let sumaDobles = nums.filter(x => x % 2 === 0).map(x => x * 2).reduce((acc, x) => acc + x, 0);</code></pre>
  </ul>
</body>
</html>

