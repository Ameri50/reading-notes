# ¿Cuáles son las principales características de Bootstrap que lo hacen ideal para el desarrollo de sitios web responsivos?

- Sistema de rejilla (Grid System): Utiliza una rejilla flexible de 12 columnas basada en CSS Flexbox, que permite crear diseños responsivos ajustándose automáticamente a diferentes tamaños de pantalla.

- Componentes prefabricados: Ofrece componentes como botones, menús de navegación, barras de progreso, tarjetas y modales, que pueden integrarse fácilmente.
Compatibilidad con navegadores: Garantiza una visualización coherente en los navegadores más populares.

- Clases utilitarias: Proporciona una amplia variedad de clases listas para usar, como márgenes, paddings, colores y alineaciones, para agilizar el diseño.

- Diseño mobile-first: Está diseñado para priorizar la experiencia en dispositivos móviles, asegurando que los sitios se vean y funcionen bien en pantallas pequeñas antes de escalar a pantallas más grandes.

## ¿Cómo facilita Bootstrap la personalización de estilos en comparación con el desarrollo CSS desde cero?

- Variables de Sass: Permite personalizar colores, fuentes, tamaños y más mediante variables definidas en Sass, lo que brinda control total sobre el diseño.

- Sobrescritura de clases: Puedes agregar tus propias reglas CSS para sobrescribir o complementar las predeterminadas.

- Temas personalizados: Bootstrap soporta la creación de temas personalizados mediante la compilación de sus archivos Sass.

- Sistema modular: Puedes importar únicamente las partes de Bootstrap que necesitas (por ejemplo, solo el sistema de rejilla o componentes específicos), reduciendo el peso del sitio y mejorando la carga.

- En comparación con CSS desde cero, Bootstrap proporciona una base estructurada y componentes ya diseñados, ahorrando tiempo y esfuerzo en tareas repetitivas como la creación de estilos base y el diseño responsivo.


### ¿Qué es jQuery y cuál es su principal objetivo en el desarrollo web?

- jQuery es una biblioteca de JavaScript ligera que simplifica la manipulación del DOM (Document Object Model), el manejo de eventos, la creación de animaciones y la realización de solicitudes AJAX.

- Principal objetivo: Hacer que las tareas de desarrollo web sean más rápidas, intuitivas y compatibles entre navegadores, permitiendo a los desarrolladores centrarse en la funcionalidad sin preocuparse por las discrepancias entre diferentes navegadores.

#### ¿Por qué se dice que jQuery permite “escribir menos y hacer más”?

- Sintaxis simplificada: jQuery reduce la cantidad de código necesario para realizar tareas comunes. Por ejemplo, seleccionar elementos del DOM o agregar un evento puede hacerse con una línea de código, en comparación con varias líneas en JavaScript puro.

- Ejemplo:

- JavaScript puro:

- document.getElementById('element').addEventListener('click', function() {
    alert('Clicked!');
});

- jQuery:

- $('#element').click(function() {
    alert('Clicked!');
});

- Compatibilidad entre navegadores: jQuery maneja las inconsistencias entre navegadores, ahorrando tiempo al desarrollador.

- Funcionalidades preintegradas: Incluye métodos para realizar tareas complejas, como animaciones o solicitudes AJAX, con una sintaxis sencilla.

- Extensibilidad: Su ecosistema de plugins permite agregar nuevas funcionalidades sin necesidad de escribir todo desde cero.

- Estas características hacen de jQuery una herramienta poderosa para desarrollar de manera eficiente.
