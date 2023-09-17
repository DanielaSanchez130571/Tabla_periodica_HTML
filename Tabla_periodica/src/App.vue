<script >

import ElementosGitHub from './components/ElementosGitHub.vue'

export default {
    components: {
        ElementosGitHub,
    }

};


</script>

<template>
    <body>
        <nav class="fondo-negro text-center">
        <div class="container-fluid">
            <h1 class="titulo display-4 pt-3">TABLA PERIODICA</h1>
        </div>
        <div class="container-fluid">
            <h1 class="titulo display-4 pb-3">
                <span class="titulo__E">E</span>
                <span class="titulo__L">L</span>
                <span class="titulo__E_2">E</span>
                <span class="titulo__M">M</span>
                <span class="titulo__E_3">E</span>
                <span class="titulo__N">N</span>
                <span class="titulo__T">T</span>
                <span class="titulo__O">O</span>
                <span class="titulo__S">S</span> HTML
            </h1>
        </div>
    </nav>

        <div id="app">
            <ElementosGitHub />
        </div>

        <!-- <div class="key wrapper">
                <div class="raw ">
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
            </div> -->

        <div class="wrapper container">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/informacion">
                <h3>Saber mas sobre HTML</h3>
            </RouterLink>
            <RouterView />
        </div>

        <footer class="text-center py-4 div-footer text-white">
        <div class="container">
            <ul class="nav justify-content-center border-bottom pb-3 mb-3">
                <li class="nav-item texto-footer"><a href="#" class="px-2 link-footer">About us</a></li>
            </ul>
            <p class="text-center ">© 2023 Kuepa - equipo 4 | México</p>
        </div>
    </footer>

    </body>
</template>

<style>
:root {
    --color-azul-claro: #69C6E5;
    --color-azul-rey: #0D88C1;
    --color-rosa-morado: #CE58AE;
    --color-fucsia: #BF058C;
    --color-rosa-mexicano: #DE0063;
    --color-salmon: #FD6885;
    --color-naranja: #FA8C33;
    --color-verde-limon: #B5CD2D;
    --color-verde: #098348;
    --color-azul-verde: #09CF9E;
    --color-amarillo-naranja: #F3B110;
    --color-marron: #CD7C3B;
    --color-nude: #FDB18E;
    --color-morado-nude: #B08D91;
    --color-gris: #D9D9D9;
    --color-negro: #0F0B0B;
    --color-blanco: #fdfdfd;
}

body {
    display: flex;
    flex-direction: column;
    min-height: 100vh; 
    margin: 0;
}

/* Navbar */
.titulo{
    color: var(--color-blanco);
    text-align: center;
    line-height: 1.5;
}

.fondo-negro{
    background-color: var(--color-negro); 
    margin-bottom: 30px; 
}

.titulo__E{
    color: var(--color-azul-claro);
}

.titulo__L{
    color: var(--color-azul-rey);
}

.titulo__E_2{
    color: var(--color-fucsia);
}

.titulo__M{
    color: var(--color-rosa-mexicano);
}

.titulo__E_3{
    color: var(--color-salmon);
}

.titulo__N{
    color: var(--color-naranja);
}

.titulo__T{
    color: var(--color-verde-limon);
}

.titulo__O{
    color: var(--color-azul-verde);
}

.titulo__S{
    color: var(--color-verde);
}
/* Footer */
.div-footer{
    background-color: var(--color-negro);
    margin-top: 30px;
}

.texto-footer{
    color: var(--color-blanco);
    
}

.link-footer {
    text-decoration: none; /* Elimina la decoración de subrayado */
    color: inherit; /* Hereda el color del texto del elemento padre (en este caso, blanco) */
}
</style>