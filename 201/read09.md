# Prototipos y Herencia en JavaScript

## ¿Qué es un prototipo en JavaScript y cómo se relaciona con la herencia?

Un **prototipo** en JavaScript es un objeto del cual otros objetos pueden heredar propiedades y métodos. Cada objeto tiene una propiedad interna llamada `[[Prototype]]`, que permite implementar la **herencia** a través de la cadena de prototipos.

### Ejemplo de Cadena de Prototipos

```javascript
function Animal(nombre) {
    this.nombre = nombre;
}

Animal.prototype.hablar = function() {
    console.log(`${this.nombre} hace un ruido.`);
};

function Perro(nombre) {
    Animal.call(this, nombre); // Llama al constructor de Animal
}

Perro.prototype = Object.create(Animal.prototype); // Hereda de Animal
Perro.prototype.constructor = Perro;

Perro.prototype.hablar = function() {
    console.log(`${this.nombre} ladra.`);
};

const miPerro = new Perro("Rex");
miPerro.hablar(); // "Rex ladra."
