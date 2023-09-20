<script>
import { ref, onMounted } from 'vue';
import { Modal } from 'bootstrap'; // Importa el módulo Modal de Bootstrap

export default {
    setup() {
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

        // Función para abrir el modal
        const openModal = (index) => {
            const modal = new Modal(document.getElementById(`modalInfo${index}`));
            modal.show();
        };

        return {
            posts,
            openModal, // Asegúrate de exponer la función openModal en el objeto de retorno
        };
    },
};
</script>

<template>
    <div class="app container mb-5">
        <section class="grid-tabla section-tabla wrapper ">
            <div class="div-elemento" v-for="(post, index) in posts" :style="{ gridColumn: post.col, gridRow: post.row }"
                :key="index">
                <div class="grid-item">
                    <div class="element">
                        <button type="button" :class="post.clasificacion" :data-bs-target="'#modalInfo' + index"
                            class="btn-elemento" @click="openModal(index)">
                            <div class="element-number">{{ post.numero }}</div>
                            <div class="label">
                                <div class="nombre">{{ post.nombre }}</div>
                                <div class="tag">{{ post.tag }}</div>
                            </div>
                        </button>
                    </div>
                </div>
                <div class="modal fade" :id="'modalInfo' + index" tabindex="-1" aria-labelledby="exampleModalLabel"
                    aria-hidden="true">
                    <div class="modal-dialog modal-dialog-centered modal-elemento">
                        <div class="modal-content">
                            <div class="modal-header " :style="{ backgroundColor: post.color }">
                                <h5 class="modal-title" id="exampleModalLabel"> </h5>
                                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>
                            <div class="modal-body">
                                <p>Nombre: <strong> {{ post.nombre }} </strong>
                                    </p>
                                <p>Tag: {{ post.tag }}</p>
                                <p>Grupo: {{ post.grupo }}</p>
                                <div>
                                    <p> Ejemplo: </p>
                                    <p class="text-center">
                                        <code style="color: black; font-weight: 600;">
                                                                    {{ post.info.ejemplo }}
                                                                </code>
                                    </p>
                                </div>
                                <p>Interfaz: <br> {{ post.info.interfazDOM }}</p>
                                <p>Referencia: <br>
                                     <a :href="post.info.URL" target="_blank">{{ post.info.URL }}</a></p>
                            </div>
                            <div class="modal-footer ">
                                <button type="button" class="btn " data-bs-dismiss="modal"
                                    :style="{ backgroundColor: post.color }">Cerrar</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
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

/* Elemento */

.btn-elemento {
    width: 60px;
    height: 60px;
}

.element {
    position: relative;
    cursor: pointer;
    transition: 500ms;
    box-sizing: border-box;
}

.element-number {
    font-size: 9px;
    color: var(--color-negro);
}

.nombre {
    font-size: 18px;
    font-weight: bold;
    color: var(--color-negro);
}

.tag {
    font-size: 10px;
}

/* Grupos */

.documentoC {
    background-color: var(--color-azul-claro);
    border-color: var(--color-azul-claro);
    border-radius: 10px;
}

.metadatoC {
    background-color: var(--color-azul-rey);
    border-color: var(--color-azul-rey);
    border-radius: 10px;

}

.listaC {
    background-color: var(--color-rosa-morado);
    border-color: var(--color-rosa-morado);
    border-radius: 10px;
}

.agrupacionC {
    background-color: var(--color-fucsia);
    border-color: var(--color-fucsia);
    border-radius: 10px;
}

.textualC {
    background-color: var(--color-rosa-mexicano);
    border-color: var(--color-rosa-mexicano);
    border-radius: 10px;
}

.multimedicaC {
    background-color: var(--color-salmon);
    border-color: var(--color-salmon);
    border-radius: 10px;
}

.tablaC {
    background-color: var(--color-naranja);
    border-color: var(--color-naranja);
    border-radius: 10px;
}

.formularioC {
    background-color: var(--color-verde-limon);
    border-color: var(--color-verde-limon);
    border-radius: 10px;
}

.scriptingC {
    background-color: var(--color-verde);
    border-color: var(--color-verde);
    border-radius: 10px;
}

.interactivaC {
    background-color: var(--color-azul-verde);
    border-color: var(--color-azul-verde);
    border-radius: 10px;
}

.semanticaC {
    background-color: var(--color-amarillo-naranja);
    border-color: var(--color-amarillo-naranja);
    border-radius: 10px;
}

.ideograficaC {
    background-color: var(--color-marron);
    border-color: var(--color-marron);
    border-radius: 10px;
}

.edicioneC {
    background-color: var(--color-nude);
    border-color: var(--color-nude);
    border-radius: 10px;
}

.obsoletaC {
    background-color: var(--color-morado-nude);
    border-color: var(--color-morado-nude);
    border-radius: 10px;
}

/* Modal */
.modal-referencia {
    font-size: 10px;
}



.modal-elemento {
    text-align: justify;
    font-size: 14px;
    max-width: 50%; /* Establece el ancho máximo al 100% del contenedor padre */
    margin: 0 auto; 
}

/* Grid  */

.section-tabla {
    flex: 1;
}

.grid-tabla {
    display: grid;
    grid-template-columns: repeat(17, 1fr);
    grid-gap: 5px;
}

.grid-item {
    text-align: center;
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

/* Media Query para  mobil */
@media screen and (max-width: 767px) {
    .grid-tabla {
        display: flex;
        flex-direction: column;
    }

    .btn-elemento {
        width: 80%;
        height: 65px;

    }
}

@media screen and (min-width: 768px) and (max-width: 1023px) {
    .grid-tabla {
        display: flex;
        flex-direction: column;
    }

    .btn-elemento {
        width: 100%;
        height: 80px;
    }
}

@media screen and (min-width: 1024px) and (max-width: 1199px) {
    .grid-tabla {
        grid-template-columns: repeat(18, 1fr);
        /* Cambia el número de columnas según tu diseño */
        grid-gap: 1;
        /* Ajusta el espacio entre elementos según sea necesario */
    }

    .btn-elemento {
        width: 50px;
        height: 50px;
    }



    .element-number {
        font-size: 6px;
        color: var(--color-negro);
    }

    .nombre {
        font-size: 10px;
        font-weight: bold;
        color: var(--color-negro);
    }

    .tag {
        font-size: 10px;
    }
}
</style>

