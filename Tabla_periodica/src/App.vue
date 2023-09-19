<script >

// import ElementosGitHub from './components/ElementosGitHub.vue'

// export default {
//     components: {
//         ElementosGitHub,
//     }

// };


</script>

<template>
    <body>
        <nav class="fondo-negro text-center">
            <div class="container-fluid">
                <h1 class="titulo display-4 pt-3">TABLA PERIÓDICA</h1>
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


            

        <div class="wrapper container">
            <RouterLink to="/"></RouterLink>
            <RouterLink to="/informacion">
                <h3>¿Qué es HTML?</h3>
            </RouterLink>
            <RouterLink to="/app">
                <h3>Tabla interactiva</h3>
            </RouterLink>
            
            <RouterView />
        </div>

        <footer class="text-center py-4 div-footer text-white">
            <div class="container">
                <ul class="nav justify-content-center border-bottom pb-3 mb-3">
                    <li class="nav-item texto-footer"><a href="#" class="px-2 link-footer">About us</a></li>
                </ul>
                <p class="text-center ">© 2023 Kuepa, TechPower - México | Equipo 4</p>
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
.titulo {
    color: var(--color-blanco);
    text-align: center;
    line-height: 1.5;
}

.fondo-negro {
    background-color: var(--color-negro);
    margin-bottom: 30px;
}

.titulo__E {
    color: var(--color-azul-claro);
}

.titulo__L {
    color: var(--color-azul-rey);
}

.titulo__E_2 {
    color: var(--color-fucsia);
}

.titulo__M {
    color: var(--color-rosa-mexicano);
}

.titulo__E_3 {
    color: var(--color-salmon);
}

.titulo__N {
    color: var(--color-naranja);
}

.titulo__T {
    color: var(--color-verde-limon);
}

.titulo__O {
    color: var(--color-azul-verde);
}

.titulo__S {
    color: var(--color-verde);
}

/* Footer */
.div-footer {
    background-color: var(--color-negro);
    margin-top: 30px;
}

.texto-footer {
    color: var(--color-blanco);

}

.link-footer {
    text-decoration: none;
    /* Elimina la decoración de subrayado */
    color: inherit;
    /* Hereda el color del texto del elemento padre (en este caso, blanco) */

    /* Interactiviada */

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

    .element input[type="radio"].activate:checked {
        z-index: 3;
        transform: scale(3);
        transition-duration: 500ms, 0ms, 200ms, 200ms, 200ms, 200ms;
        transition-delay: 0ms;
        outline: none;
        cursor: auto;
    }

    .element input[type="radio"].activate:checked~.label {
        transition-duration: 500ms;
        transform: scale(0.75);
    }

    .element input[type="radio"].activate:checked {
        opacity: 1;
        transition: 500ms;
    }

    .element input[type="radio"].activate:checked~ {
        display: block;
        animation: fade-in;
        animation-duration: 1s;
    }

    .element input[type="radio"].activate:checked~ {
        animation-name: rotate;
        animation-timing-function: linear;
        animation-iteration-count: infinite;
    }

    .element input[type="radio"].deactivate {
        position: fixed;
        display: block;
        z-index: 1;
        opacity: 0;
        pointer-events: none;
    }

    .element input[type="radio"].deactivate:checked~ {
        z-index: 1;
    }

    .raw {
        position: relative;
        display: flex;
        width: 100%;
        justify-content: space-between;
    }


    .key .raw label:hover {
        opacity: 1 !important;
    }

    .raw label:hover {
        opacity: 1 !important;
    }

    .categorias {
        background-color: var(--color-gris);
        padding: 10px;
        border-radius: 10px;

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

}</style>