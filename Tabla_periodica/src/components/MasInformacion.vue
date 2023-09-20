<template>
  <div class="informacion container">
    <h1 class="text-center mt-3">
      <strong>
        <span class="titulo__L">LENGUAJE</span>
        <span class="titulo__M"> DE</span>
        <span class="titulo__N "> ETIQUETAS</span>
        <span class="titulo__O"> DE</span>
        <span class="titulo__S"> HIPERTEXTO</span>
      </strong>
    </h1>
    <p class="mt-5">HTML, cuya sigla proviene del inglés "HyperText Markup Language" (Lenguaje de Marcado de Hipertexto),
      representa el componente fundamental de la World Wide Web. Para comprender su esencia, desglosemos sus elementos
      constituyentes:
    </p>
    <ul>
      <li><strong> Hipertexto (Hypertext):</strong> Este término se refiere a texto, generalmente en forma de enlaces, que
        se encuentra
        organizado de manera que establece conexiones entre elementos relacionados.</li>
      <li><strong> Marcado (Markup):</strong>
        Se trata de una pauta de estilo que se utiliza para representar elementos que serán visualizados en el navegador
        de manera gráfica.</li>
      <li><strong>Lenguaje (Language):</strong>
        En este contexto, se refiere a un idioma que es entendido por las computadoras y que se emplea para interpretar
        comandos.</li>
    </ul>
    <p>Un documento HTML básico comienza con una etiqueta <code>&lt;html&gt;</code> que envuelve todo el contenido de la
      página. Dentro del <code>&lt;html&gt;</code>, hay secciones como <code>&lt;head&gt;</code> para metadatos y
      <code>&lt;body&gt;</code> para el contenido visible de la página.
    </p>
    <p>
      HTML permite definir tanto la estructura como el contenido de una página web utilizando etiquetas y atributos que
      proporcionan instrucciones al navegador sobre cómo mostrar la información.
    </p>
    <p>
      En su esencia, HTML emplea etiquetas para describir los diversos componentes de una página web. Estas etiquetas son
      códigos que guían al navegador en la representación del contenido
    </p>
    <p>
      La sintaxis de HTML es directa: se compone de una serie de etiquetas y atributos que se escriben en un archivo de
      texto plano con extensión .html. Cada etiqueta se encierra entre corchetes angulares y algunas de ellas pueden
      incluir atributos definidos dentro de la propia etiqueta.
    </p>
    <p>
      Los atributos se incorporan en la etiqueta de apertura y pueden pertenecer a distintos tipos, como "style," "id,"
      "class," y otros más. Estos atributos llevan consigo valores que proporcionan información adicional a un elemento,
      permitiendo la adición de estilos o la creación de interactividad con tecnologías como CSS, Bootstrap, JavaScript,
      entre otras.
    </p>
    <p>
      Una de las principales funciones de HTML radica en atribuir significado al texto, un concepto conocido como
      semántica, lo que capacita al navegador para presentar el contenido de manera adecuada. Una ventaja considerable de
      utilizar etiquetas semánticamente correctas radica en que los motores de búsqueda web (web crawlers) pueden indexar
      con facilidad las páginas y los sitios web, lo que conlleva una mejora en el
      <strong> SEO</strong>
      (Optimización de Motores de
      Búsqueda)
    </p>
    <p>
      <strong> HTML 5 </strong>
      representa la versión más reciente de este lenguaje de programación, lanzada en octubre de 2014 por el
      consorcio
      <strong> W3C. </strong>
      Esta actualización moderniza el lenguaje reemplazando etiquetas obsoletas por versiones actualizadas
      y aprovechando las últimas tecnologías y demandas web, como formularios, visualizadores, manejo de grandes conjuntos
      de datos, entre otros
    </p>
    <p>
      En resumen, HTML, o Lenguaje de Marcado de Hipertexto, es el pilar fundamental de la <strong> World Wide Web.ƒ
      </strong>
      Su capacidad
      para definir la estructura y el contenido de las páginas web mediante etiquetas y atributos es esencial para la
      creación y presentación de información en línea. Al utilizar etiquetas semánticamente correctas, HTML no solo
      permite que los navegadores muestren el contenido de manera apropiada, sino que también mejora la indexación de las
      páginas web por parte de los motores de búsqueda, lo que contribuye a un mejor rendimiento en términos de SEO.
    </p>
    <p>
      La evolución constante de HTML, con HTML5 como su versión más reciente, garantiza que el lenguaje se mantenga al día
      con las necesidades cambiantes de la web y aproveche las últimas tecnologías y funcionalidades. En última instancia,
      HTML es el cimiento sobre el cual se construyen y desarrollan las experiencias en línea, permitiendo a los
      diseñadores y desarrolladores web crear contenido interactivo y atractivo para los usuarios de todo el mundo.
    </p>


  </div>
</template>

<style>
@font-face {
  font-family: 'Montserrat';
  src: url('./src/assets/tipografias/Montserrat/Montserrat-VariableFont_wght.ttf') format('truetype');
}

.informacion {
  font-family: 'Montserrat';
  text-align: justify;
  line-height: 2;
}

.titulo__L {
  color: var(--color-azul-rey);
}



.titulo__M {
  color: var(--color-rosa-mexicano);
}


.titulo__N {
  color: var(--color-naranja);
}

.titulo__O {
  color: var(--color-azul-verde);
}

.titulo__S {
  color: var(--color-verde);
}

/* Estilos para pantallas grandes (más de 1024px de ancho) */
@media (min-width: 1025px) {
  .informacion {
    min-height: 100vh;
    display: flex;
    align-items: center;
    font-size: large;
  }
}

/* Estilos para pantallas medianas (entre 768px y 1024px de ancho) */
@media (min-width: 768px) and (max-width: 1024px) {
  .informacion {
    font-size: medium;
  }
}

/* Estilos para pantallas pequeñas (menos de 768px de ancho) */
@media (max-width: 767px) {
  .informacion {
    font-size: small;
  }
}

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