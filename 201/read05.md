<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Conceptos</title>
</head>
<body>
  <h1>Conceptos clave de JavaScript</h1>

  <h2>Estructuras condicionales</h2>
  <ul>
    <li><strong>if/else:</strong> Para decisiones simples o con pocas condiciones.</li>
    <pre><code>if (x > 10) console.log("Mayor a 10"); else console.log("Menor o igual a 10");</code></pre>

    <li><strong>switch:</strong> Para comparar un valor específico entre múltiples casos.</li>
    <pre><code>switch (day) { case 1: console.log("Lunes"); break; }</code></pre>

    <li><strong>Operador ternario:</strong> Para condiciones cortas en una línea.</li>
    <pre><code>let result = x > 10 ? "Mayor" : "Menor";</code></pre>
  </ul>

  <h2>Métodos de arreglos</h2>
  <ul>
    <li><strong>push():</strong> Agrega al final del arreglo.</li>
    <pre><code>arr.push(4); // [1, 2, 3, 4]</code></pre>

    <li><strong>unshift():</strong> Agrega al inicio del arreglo.</li>
    <pre><code>arr.unshift(0); // [0, 1, 2, 3]</code></pre>

    <li><strong>splice():</strong> Inserta, reemplaza o elimina elementos en cualquier posición.</li>
    <pre><code>arr.splice(1, 0, "nuevo"); // [1, "nuevo", 2, 3]</code></pre>
  </ul>

  <h2>Diferencias entre bucles</h2>
  <ul>
    <li><strong>for:</strong> Para iteraciones conocidas o controladas.</li>
    <pre><code>for (let i = 0; i < arr.length; i++) console.log(arr[i]);</code></pre>

    <li><strong>while:</strong> Para repetir mientras se cumple una condición.</li>
    <pre><code>while (x < 10) { console.log(x); x++; }</code></pre>

    <li><strong>do...while:</strong> Asegura al menos una ejecución.</li>
    <pre><code>do { console.log(x); x++; } while (x < 10);</code></pre>
  </ul>

  <h2>Recorrer un arreglo</h2>
  <ul>
    <li><strong>for:</strong> Más control, útil si necesitas el índice.</li>
    <li><strong>forEach():</strong> Simplifica recorrer elementos.</li>
    <pre><code>arr.forEach(el => console.log(el));</code></pre>

    <li><strong>for...of:</strong> Elegante para recorrer elementos directamente.</li>
    <pre><code>for (let el of arr) console.log(el);</code></pre>

    <li><strong>map():</strong> Transforma elementos creando un nuevo arreglo.</li>
    <pre><code>let doubled = arr.map(x => x * 2);</code></pre>
  </ul>

  <p><strong>Eficiencia:</strong> Usa <code>for</code> para control fino, <code>forEach()</code> o <code>for...of</code> para lecturas simples, y <code>map()</code> para transformaciones.</p>
</body>
</html>

