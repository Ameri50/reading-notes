<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Programación Orientada a Objetos en JavaScript</title>
</head>
<body>
  <h1>Conceptos de Programación Orientada a Objetos en JavaScript</h1>

  <h2>¿Qué es la abstracción en programación?</h2>
  <p><strong>Definición:</strong> La abstracción es el proceso de ocultar los detalles internos y exponer solo lo esencial para simplificar el uso de un objeto o clase.</p>
  <p><strong>Implementación en JavaScript:</strong> Usamos métodos y propiedades públicas para exponer funcionalidades clave, mientras que los detalles internos se mantienen privados.</p>
  <pre><code>// Ejemplo de abstracción
class CuentaBancaria {
  #saldo; // Propiedad privada

  constructor(saldoInicial) {
    this.#saldo = saldoInicial;
  }

  depositar(cantidad) {
    this.#saldo += cantidad;
  }

  obtenerSaldo() {
    return this.#saldo; // Solo se accede a través de este método
  }
}

const cuenta = new CuentaBancaria(100);
cuenta.depositar(50);
console.log(cuenta.obtenerSaldo()); // 150</code></pre>

  <h2>Los cuatro pilares de la Programación Orientada a Objetos</h2>
  <ul>
    <li><strong>Abstracción:</strong> Oculta detalles innecesarios (ver ejemplo arriba).</li>
    <li><strong>Encapsulación:</strong> Protege los datos internos y solo expone métodos controlados.
      <pre><code>class Persona {
  #nombre;
  constructor(nombre) {
    this.#nombre = nombre;
  }
  obtenerNombre() {
    return this.#nombre;
  }
}</code></pre>
    </li>
    <li><strong>Herencia:</strong> Permite que una clase hija reutilice las propiedades y métodos de una clase padre (ver ejemplo más adelante).</li>
    <li><strong>Polimorfismo:</strong> Permite usar un mismo método en clases diferentes con comportamientos personalizados.
      <pre><code>class Animal {
  hacerSonido() {
    console.log("Sonido genérico");
  }
}

class Perro extends Animal {
  hacerSonido() {
    console.log("Ladrido");
  }
}

const animal = new Animal();
const perro = new Perro();
animal.hacerSonido(); // "Sonido genérico"
perro.hacerSonido();  // "Ladrido"</code></pre>
    </li>
  </ul>

  <h2>Objeto literal vs Clase</h2>
  <p><strong>Objeto literal:</strong> Es una forma sencilla y directa de crear un objeto. Útil para estructuras de datos pequeñas o específicas.</p>
  <pre><code>const persona = {
  nombre: "Juan",
  saludar: function() {
    console.log(`Hola, soy ${this.nombre}`);
  }
};
persona.saludar(); // "Hola, soy Juan"</code></pre>

  <p><strong>Clase:</strong> Es una plantilla para crear objetos más complejos con lógica estructurada. Ideal para sistemas más grandes y reutilizables.</p>
  <pre><code>class Persona {
  constructor(nombre) {
    this.nombre = nombre;
  }
  saludar() {
    console.log(`Hola, soy ${this.nombre}`);
  }
}
const persona = new Persona("Juan");
persona.saludar(); // "Hola, soy Juan"</code></pre>

  <h2>¿Cuándo usar cada uno?</h2>
  <ul>
    <li>Usa <strong>objeto literal</strong> para casos simples, como configuraciones o datos estáticos.</li>
    <li>Usa <strong>clase</strong> cuando necesitas una estructura más robusta con lógica encapsulada y reutilizable.</li>
  </ul>

  <h2>Implementación de herencia en JavaScript</h2>
  <pre><code>// Clase padre
class Animal {
  constructor(nombre) {
    this.nombre = nombre;
  }
  hacerSonido() {
    console.log(`${this.nombre} hace un sonido.`);
  }
}

// Clase hija
class Perro extends Animal {
  hacerSonido() {
    console.log(`${this.nombre} ladra.`);
  }
}

const perro = new Perro("Fido");
perro.hacerSonido(); // "Fido ladra."</code></pre>

</body>
</html>

