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
                <h1 class="titulo display-4 pt-5">TABLA PERIÓDICA</h1>
            </div>
            <div class="container-fluid">
                <h1 class="titulo display-4 pb-2">
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
            <div class="container">
                <nav class="navbar navbar-expand-lg navbar-light">
                    <ul class="navbar-nav custom-nav">
                        <!-- Ítem a la izquierda -->
                        <li class="nav-item">
                            <RouterLink to="/app" class="nav-link text-white">
                                <h4>Tabla interactiva</h4>
                            </RouterLink>
                        </li>
                        <li class="nav-item">
                            <RouterLink to="/" class="nav-link text-white">
                                <h4>Home</h4>
                            </RouterLink>
                        </li>
                        <!-- Ítem a la derecha -->
                        <li class="nav-item">
                            <RouterLink to="/informacion" class="nav-link text-white co">
                                <h4>¿Qué es HTML?</h4>
                            </RouterLink>
                        </li>
                    </ul>
                </nav>
            </div>
        </nav>

        <RouterView />




        <footer class="text-center py-4 mt-5 div-footer text-white">
            <div class="container">
                <ul class="nav justify-content-center border-bottom pb-3 mb-3">
                    <li class="nav-item texto-footer">
                        <RouterLink to="/us" class="nav-link text-white">
                                about us
                            </RouterLink>
                    </li>
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

@font-face {
    font-family: 'Rubik';
    src: url('./src/assets/tipografias/Rubik_80s_Fade/Rubik80sFade-Regular.ttf') format('truetype');
}

@font-face {
    font-family: 'Montserrat';
    src: url('./src/assets/tipografias/Montserrat/Montserrat-VariableFont_wght.ttf') format('truetype');
}

body {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    margin: 0;
    font-family: 'Montserrat';
}

/* Navbar */
.titulo {
    color: var(--color-blanco);
    text-align: center;
    line-height: 1.5;
    font-family: 'Rubik'
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

.custom-nav {
    display: flex;
    justify-content: space-between;
    width: 100%;
}

.custom-nav .nav-item {
    flex: 1;
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
    color: inherit;
}

/* Querys */

@media (min-width: 992px) {
  .titulo.display-4 {
    font-size: 2.5rem;
  }

  /* Agrega más ajustes de estilo para pantallas grandes aquí */
}

@media (max-width: 991px) {
  .titulo.display-4 {
    font-size: 2rem;
  }

  /* Agrega más ajustes de estilo para pantallas medianas aquí */
}

@media (max-width: 767px) {
  .titulo.display-4 {
    font-size: 1.5rem;
  }
}
</style>