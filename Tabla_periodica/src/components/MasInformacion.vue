<template>
    <div class="informacion">
        <h1>¿Qué es HTML?</h1>
        <p>HTML (HyperText Markup Language) es un lenguaje de marcado utilizado para crear la estructura y el contenido de páginas web. Se trata de un lenguaje de programación ligero y esencialmente un estándar de la World Wide Web (WWW) que permite a los desarrolladores web definir la estructura y organización de una página web mediante etiquetas y elementos.</p>
        <br>
        <p>Aquí hay algunas características clave de HTML:</p>
        <ul>
            <li>Marcado de contenido: HTML se utiliza para marcar o etiquetar el contenido de una página web. Esto significa que se utilizan etiquetas HTML para definir qué parte del contenido es un encabezado, un párrafo, una lista, una imagen, un enlace y más.</li>
            <li>Estructura jerárquica: Las etiquetas HTML se organizan jerárquicamente, lo que significa que algunos elementos pueden contener otros elementos. Esta jerarquía ayuda a definir la estructura de la página web.</li>
            <li>Interconexión: HTML permite enlazar páginas web mediante hipervínculos o enlaces. Esto es fundamental para la navegación en la web.</li>
            <li>Compatibilidad: Los navegadores web interpretan y renderizan el código HTML, lo que significa que las páginas web escritas en HTML se pueden ver y navegar en una variedad de dispositivos y plataformas.</li>
        </ul>
        <p>Un documento HTML básico comienza con una etiqueta <code>&lt;html&gt;</code> que envuelve todo el contenido de la página. Dentro del <code>&lt;html&gt;</code>, hay secciones como <code>&lt;head&gt;</code> para metadatos y <code>&lt;body&gt;</code> para el contenido visible de la página.</p>
    </div>
</template>

<style>
@media (min-width: 1024px) {
  .informacion {
    min-height: 100vh;
    display: inline-block;
    align-items: center;
    font-size: large;
    font-family: sans-serif;
  }
}
</style>