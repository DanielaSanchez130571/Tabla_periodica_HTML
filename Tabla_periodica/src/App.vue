<script >

import ElementosGitHub from './components/ElementosGitHub.vue'

export default {
    components: {
        ElementosGitHub
    }

};
</script>

<template>
    <body>
        <nav class="navBar">
            <h1 class="titulo">TABLA PERIÓDICA</h1>
            <h1 class="titulo">
                <span class="eTitulo">E</span>
                <span class="lTitulo">L</span>
                <span class="eTitulo2">E</span>
                <span class="mTitulo">M</span>
                <span class="eTitulo3">E</span>
                <span class="nTitulo">N</span>
                <span class="tTitulo">T</span>
                <span class="oTitulo">O</span>
                <span class="sTitulo">S</span> HTML
            </h1>
        </nav>

        <div id="app">
            <ElementosGitHub />
        </div>

        <div class="key wrapper">
                <div class="row">
                    <label class="docuemntoC categorias" for="documentosC">Documento</label>
                    <label class="metadatoC categorias" for="metadatosC">Metadatos</label>
                    <label class="listaC categorias" for="listasC">Listas</label>
                    <label class="agrupacionC categorias" for="agrupacionesC">Agrupación</label>
                    <label class="textualC categorias" for="textualesC">Textual</label>
                    <label class="multimedicaC categorias" for="multimedicasC">Multimedia</label>
                    <label class="tablaC categorias" for="tablasC">Tablas</label>
                    <label class="formularioC categorias" for="formulariosC">Formulario</label>
                    <label class="scriptingC categorias" for="scriptingsC">Scripting</label>
                    <label class="interactivaC categorias" for="interactivasC">Interactivas</label>
                    <label class="semanticaC categorias" for="semanticasC">Semánticas</label>
                    <label class="ideograficaC categorias" for="ideograficasC">Ideográficas</label>
                    <label class="edicionC categorias" for="edicionesC">Edición</label>
                    <label class="obsoletaC categorias" for="obsoletasC">Obsoletas</label>
                </div>
            </div>

        <div class="wrapper">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/informacion">
                <h3>Saber mas sobre HTML</h3>
            </RouterLink>
            <RouterView />
        </div>

        <footer class="footer">
            <p>&copy; 2023 | Kuepa | TechPower</p>
        </footer>

    </body>
</template>