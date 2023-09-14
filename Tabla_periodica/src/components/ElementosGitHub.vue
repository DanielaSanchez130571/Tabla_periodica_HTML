<script setup>
import { ref, onMounted } from 'vue';

const posts = ref([]);

const getData = async () => {
    try {
        const res = await fetch('https://raw.githubusercontent.com/DanielaSanchez130571/AppyTabla/main/elementos.json');
        const data = await res.json();
        posts.value = data;
        console.log(posts.value);
    } catch (error) {
        console.error(error);
    }
};

onMounted(() => {
    getData();
});
</script>


    <!-- <ElementosGitHub v-for="post in posts" :key="numero" :numero="post.numero" :nombre="post.nombre" :tag="post.tag"
        :grupo="post.grupo" :color="post.color" / -->

<template>
    <div class="wrapper">
        <input class="categorias-t" type="radio" id="documentosC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="metadatosC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="listasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="agrupacionesC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="textualesC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="multimedicasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="tablasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="formulariosC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="scriptingsC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="interactivasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="semanticasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="ideograficasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="edicionesC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />
        <input class="categorias-t" type="radio" id="obsoletasC" name="categories" />
        <input class="categorias-cancel" type="radio" id="cancel" name="categories" />

        <div class="periodic-table">
            <!-- col 1 -->
            <div v-for="post in posts" :key="post.numero" class="element" :style="{ gridColumn: post.col, gridRow: post.row}">
                <div class="element interactivaC c1 r1">
                    <input class="activate" type="radio" name="elements" />
                    <input class="deactivate" type="radio" name="elements" />
                    <div class="overlay"></div>
                    <div class="square" :style="{ background:post.color }">
                        <div class="atomic-number">{{ post.numero }}</div>
                        <div class="label">
                            <div class="symbol">{{ post.nombre }}</div>
                            <div class="name">{{ post.tag }}</div>
                            <div class="grupo">{{ post.grupo }}</div>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
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

.element-grid {
    display: grid;
    grid-template-columns: repeat(17, 1fr);
    /* grid-template-rows: repeat(9, 1fr); */
    /* 17 columnas */
    gap: 5px;
    /* Espacio entre elementos */
    /* Agrega otros estilos según sea necesario */
}

@font-face {
    font-family: 'Next';
    src: url('./assets/tipografias/NexaRustSlab-Trial-BlackShadow3.ttf') format('woff2');
    font-weight: normal;
    font-style: normal;
}


@media (min-width: 1200px) {
    h1 {
        font-size: 4rem;
    }

}

body {
    margin: 0;
    padding: 0;
}

.navBar {
    background-color: var(--color-negro);
    color: var(--color-blanco);
    width: 100%;
    padding: 10px 0;
    text-align: center;
}

h1 {
    font-family: 'Next';
}

.eTitulo {
    color: var(--color-azul-claro);
    font-family: 'Next';
}

.lTitulo {
    color: var(--color-azul-rey);
}

.eTitulo2 {
    color: var(--color-fucsia);
}

.mTitulo {
    color: var(--color-rosa-mexicano);
}

.eTitulo3 {
    color: var(--color-salmon);
}

.nTitulo {
    color: var(--color-naranja);
}

.tTitulo {
    color: var(--color-verde-limon);
}

.oTitulo {
    color: var(--color-azul-verde);
}

.sTitulo {
    color: var(--color-verde);
}

.footer {
    background-color: var(--color-negro);
    color: var(--color-blanco);
    padding: 10px;
    text-align: center;
    bottom: 0;
    width: 100%;
}

.documento {
    background-color: var(--color-azul-claro)
}

.metadatos {
    background-color: var(--color-azul-rey)
}

.listas {
    background-color: var(--color-rosa-morado)
}

.agrupacion {
    background-color: var(--color-fucsia)
}

.textual {
    background-color: var(--color-rosa-mexicano)
}

.multimedia {
    background-color: var(--color-salmon)
}

.tablas {
    background-color: var(--color-naranja)
}

.formulario {
    background-color: var(--color-verde-limon)
}

.scripting {
    background-color: var(--color-verde)
}

.interactivas {
    background-color: var(--color-azul-verde)
}

.semanticas {
    background-color: var(--color-amarillo-naranja)
}

.ideograficas {
    background-color: var(--color-marron)
}

.edicion {
    background-color: var(--color-nude)
}

.obsoletas {
    background-color: var(--color-morado-nude)
}

.wrapper {
    position: relative;
    overflow: hidden;
    padding: 2%;
    width: 85%;
    margin-left: 5%;
    margin-top: 3%;
}

.wrapper>input {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    visibility: hidden;
    opacity: 0;
    pointer-events: none;
}

.periodic-table {
    display: grid;
    grid-gap: 12px;
    grid-template-columns: repeat(17, 1fr);
}

.element {
    position: relative;
    font-size: 0.5vw;
    padding-bottom: 100%;
    cursor: pointer;
    color: var(--color-blanco);
    transition: 500ms;
}

.element .overlay {
    position: fixed;
    z-index: 1;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background-color: var(--color-negro);
    opacity: 0;
    pointer-events: none;
    transition: 500ms;
}

.element .square {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    box-sizing: border-box;
    color: var(--color-negro);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

}

.element .atomic-number {
    position: center;
}

.element .label {
    text-align: center;
}

.element .symbol {
    font-size: 1.7vw;
}

.element .name {
    font-size: 0.7vw;
}

code {
    color: var(--color-negro);
}

.element input[type="radio"] {
    position: absolute;
    z-index: 2;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    cursor: pointer;
    outline: none;
}

.element input[type="radio"].activate:hover~.square {
    z-index: 2;
    transform: scale(1.35);
    transition-delay: 0ms;
    outline: none;
    pointer-events: none;
}

.element input[type="radio"].activate:checked+input[type="radio"].deactivate {
    z-index: 3;
    pointer-events: all;
}

.element input[type="radio"].activate:checked~.overlay {
    opacity: 0.75;
}

.element input[type="radio"].activate:checked~.square {
    z-index: 3;
    transform: scale(3);
    transition-duration: 500ms, 0ms, 200ms, 200ms, 200ms, 200ms;
    transition-delay: 0ms;
    outline: none;
    cursor: auto;
}

/* .element input[type="radio"].activate:checked~.square .label {
        transition-duration: 500ms;
        transform: scale(0.75);
    } */

.element input[type="radio"].activate:checked~.square {
    opacity: 1;
    transition: 500ms;
}

.element input[type="radio"].activate:checked~.square .model {
    display: block;
    animation: fade-in;
    animation-duration: 1s;
}

.element input[type="radio"].deactivate {
    position: fixed;
    display: block;
    z-index: 1;
    opacity: 0;
    pointer-events: none;
}

.element input[type="radio"].deactivate:checked~.square {
    z-index: 1;
}

.placeholder {
    position: relative;
    z-index: -1;
    font-size: 1vw;
    padding-bottom: 100%;
    color: #fff;
    transition: 500ms;
}

.placeholder .square {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    border: 2px solid;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    opacity: 0.5;
}

.gap {
    position: relative;
    padding-bottom: 100%;
    transition: 500ms;
}

.gap::before {
    content: "";
    position: absolute;
    left: 50%;
    top: 0;
    width: 50%;
    height: calc(200% + 5px * 2 - 4px);
    border-width: 0 0 2px 2px;
    border-style: solid;
    margin-left: -1px;
    color: var(--color-blanco);
    opacity: 0.2;
}

@media screen and (min-width: 1024px) {
    .r1 {
        grid-row: 1;
    }

    .r2 {
        grid-row: 2;
    }

    .r3 {
        grid-row: 3;
    }

    .r4 {
        grid-row: 4;
    }

    .r5 {
        grid-row: 5;
    }

    .r6 {
        grid-row: 6;
    }

    .r7 {
        grid-row: 7;
    }

    .r8 {
        grid-row: 8;
    }

    .r9 {
        grid-row: 9;
    }

    .r10 {
        grid-row: 10;
    }

    .c1 {
        grid-column: 1;
    }

    .c2 {
        grid-column: 2;
    }

    .c3 {
        grid-column: 3;
    }

    .c4 {
        grid-column: 4;
    }

    .c5 {
        grid-column: 5;
    }

    .c6 {
        grid-column: 6;
    }

    .c7 {
        grid-column: 7;
    }

    .c8 {
        grid-column: 8;
    }

    .c9 {
        grid-column: 9;
    }

    .c10 {
        grid-column: 10;
    }

    .c11 {
        grid-column: 11;
    }

    .c12 {
        grid-column: 12;
    }

    .c13 {
        grid-column: 13;
    }

    .c14 {
        grid-column: 14;
    }

    .c15 {
        grid-column: 15;
    }

    .c16 {
        grid-column: 16;
    }

    .c17 {
        grid-column: 17;
    }


    .r1 input[type="radio"].activate:checked~.square {
        top: 100%;
    }

    .r10 input[type="radio"].activate:checked~.square {
        top: -100%;
    }

    .c1 input[type="radio"].activate:checked~.square {
        left: 100%;
    }

    .c17 input[type="radio"].activate:checked~.square {
        left: -100%;
    }
}

@media screen and (max-width: 1023px) {
    .element {
        grid-column-start: 1;
        grid-column-end: 17;
    }

    .wrapper {
        position: relative;
        overflow: hidden;
        padding: 2%;
        width: 85%;
        margin-left: 5%;
        margin-top: 3%;
    }

    .wrapper>input {
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        visibility: hidden;
        opacity: 0;
        pointer-events: none;
    }

    .periodic-table {
        display: grid;
        grid-gap: 12px;
        grid-template-columns: repeat(17, 1fr);
    }

    .element {
        position: relative;
        font-size: 0.5vw;
        padding-bottom: 100%;
        cursor: pointer;
        color: var(--color-blanco);
        transition: 500ms;
    }

    .element .overlay {
        position: fixed;
        z-index: 1;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        background-color: var(--color-negro);
        opacity: 0;
        pointer-events: none;
        transition: 500ms;
    }

    .element .square {
        position: absolute;
        left: 10%;
        top: 0;
        width: 80%;
        height: 80%;
        border-radius: 10px;
        box-sizing: border-box;
        color: var(--color-negro);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

    }

    .element .atomic-number {
        position: center;
        font-size: 5vw;
    }

    .element .label {
        text-align: center;
    }

    .element .symbol {
        font-size: 20vw;
    }

    .element .name {
        font-size: 5vw;
    }

    .r1 input[type="radio"].activate:checked~.square {
        top: 80%;
    }

    .r10 input[type="radio"].activate:checked~.square {
        top: -80%;
    }

    .c1 input[type="radio"].activate:checked~.square {
        left: 80%;
    }

    .c17 input[type="radio"].activate:checked~.square {
        left: -80%;
    }
}

@keyframes fade-in {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}

@keyframes noise {

    0%,
    100% {
        background-position: 0 0;
    }

    10% {
        background-position: -5% -10%;
    }

    20% {
        background-position: -15% 5%;
    }

    30% {
        background-position: 7% -25%;
    }

    40% {
        background-position: 20% 25%;
    }

    50% {
        background-position: -25% 10%;
    }

    60% {
        background-position: 15% 5%;
    }

    70% {
        background-position: 0% 15%;
    }

    80% {
        background-position: 25% 35%;
    }

    90% {
        background-position: -10% 10%;
    }
}

.key {
    position: relative;
    z-index: 1;
    grid-row: 1;
    grid-column-start: 3;
    grid-column-end: 17;
    font-size: 0.8vw;
    line-height: 1.5;
    display: flex;
    align-items: center;
    pointer-events: none;
    user-select: none;
}

.key .row {
    position: relative;
    display: flex;
    width: 100%;
    justify-content: space-between;
}

.key .row label {
    opacity: 0.85;
    cursor: pointer;
    transition: 120ms;
    pointer-events: all;
}

.key .row label:hover {
    opacity: 1 !important;
}

.categorias {
    background-color: var(--color-gris);
    padding: 10px;
    border-radius: 10px;
}

.docuemntoC:hover {
    background-color: var(--color-azul-claro);
}

.metadatoC:hover {
    background-color: var(--color-azul-rey);
}

.listaC:hover {
    background-color: var(--color-rosa-morado);
}

.agrupacionC:hover {
    background-color: var(--color-fucsia);
}

.textualC:hover {
    background-color: var(--color-rosa-mexicano);
}

.multimedicaC:hover {
    background-color: var(--color-salmon);
}

.tablaC:hover {
    background-color: var(--color-naranja);
}

.formularioC:hover {
    background-color: var(--color-verde-limon);
}

.scriptingC:hover {
    background-color: var(--color-verde);
}

.interactivaC:hover {
    background-color: var(--color-azul-verde);
}

.semanticaC:hover {
    background-color: var(--color-amarillo-naranja);
}

.ideograficaC:hover {
    background-color: var(--color-marron);
}

.edicionC:hover {
    background-color: var(--color-nude);
}

.obsoletaC:hover {
    background-color: var(--color-morado-nude);
}




#documentosC:checked~.periodic-table .element:not(.documentoC),
#documentosC:checked~.periodic-table .placeholder,
#metadatosC:checked~.periodic-table .element:not(.metadatoC),
#metadatosC:checked~.periodic-table .placeholder,
#listasC:checked~.periodic-table .element:not(.listaC),
#listasC:checked~.periodic-table .placeholder,
#agrupacionesC:checked~.periodic-table .element:not(.agrupacionC),
#agrupacionesC:checked~.periodic-table .placeholder,
#textualesC:checked~.periodic-table .element:not(.textualC),
#textualesC:checked~.periodic-table .placeholder,
#multimedicasC:checked~.periodic-table .element:not(.multimedicaC),
#multimedicasC:checked~.periodic-table .placeholder,
#tablasC:checked~.periodic-table .element:not(.tablaC),
#tablasC:checked~.periodic-table .placeholder,
#formulariosC:checked~.periodic-table .element:not(.formularioC),
#formulariosC:checked~.periodic-table .placeholder,
#scriptingsC:checked~.periodic-table .element:not(.scriptingC),
#scriptingsC:checked~.periodic-table .placeholder,
#interactivasC:checked~.periodic-table .element:not(.interactivaC),
#interactivasC:checked~.periodic-table .placeholder,
#semanticasC:checked~.periodic-table .element:not(.semanticaC),
#semanticasC:checked~.periodic-table .placeholder,
#ideograficasC:checked~.periodic-table .element:not(.ideograficaC),
#ideograficasC:checked~.periodic-table .placeholder,
#edicionesC:checked~.periodic-table .element:not(.edicioneC),
#edicionesC:checked~.periodic-table .placeholder,
#obsoletasC:checked~.periodic-table .element:not(.obsoletaC),
#obsoletasC:checked~.periodic-table .placeholder {
    opacity: 0.15;
    pointer-events: none;
}


#documentosC:checked~.periodic-table .key label:not(.documentoC),
#metadatosC:checked~.periodic-table .key label:not(.metadatoC),
#listasC:checked~.periodic-table .key label:not(.listaC),
#agrupacionesC:checked~.periodic-table .key label:not(.agrupacionC),
#textualesC:checked~.periodic-table .key label:not(.textualC),
#multimedicasC:checked~.periodic-table .key label:not(.multimedicaC),
#tablasC:checked~.periodic-table .key label:not(.tablaC),
#formulariosC:checked~.periodic-table .key label:not(.formularioC),
#scriptingsC:checked~.periodic-table .key label:not(.scriptingC),
#interactivasC:checked~.periodic-table .key label:not(.interactivaC),
#semanticasC:checked~.periodic-table .key label:not(.semanticaC),
#ideograficasC:checked~.periodic-table .key label:not(.ideograficaC),
#edicionesC:checked~.periodic-table .key label:not(.edicioneC),
#obsoletasC:checked~.periodic-table .key label:not(.obsoletaC) {
    opacity: 0.65;
}

.categorias-t:checked~.categorias-cancel {
    visibility: visible;
    pointer-events: all;
    cursor: pointer;
}
</style>

