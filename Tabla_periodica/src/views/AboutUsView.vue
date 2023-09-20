<template>
    <body class="container">
        <h2 class="text-center mt-2 mb-5">Nosotras </h2>
      <div class="row">
        <div class="col-md-6">
          <div class="card border-0 text-center">
            <img src="../assets/img/DS.png" class="card-img-top img-fixed-size align-self-center" alt="Daniela Sanchez">
            <div class="card-body">
              <h5 class="card-title title-us">Daniela Sanchez</h5>
              <div class="card-footer mt-4 mb-4 border-0">
                <a href="https://github.com/DanielaSanchez130571" target="_blank">
                  <img src="../assets/icons/gitHub.png" class="img-fluid icon--git" alt="github">
                </a>
                <a href="https://github.com/DanielaSanchez130571" target="_blank">
                  <img src="../assets/icons/linkedin.png" class="img-fluid icon-linked" alt="linkedIn">
                </a>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="card border-0 text-center">
            <img src="../assets/img/DHT.png" class="card-img-top img-fixed-size align-self-center" alt="Daniela Heredia">
            <div class="card-body">
              <h5 class="card-title title-us">Daniela Heredia</h5>
              <div class="card-footer mt-4 mb-4 border-0">
                <a href="https://github.com/DanHT22" target="_blank">
                  <img src="../assets/icons/gitHub.png" class="img-fluid icon--git" alt="github">
                </a>
                <a href="https://www.linkedin.com/in/daniela-heredia-t/" target="_blank">
                  <img src="../assets/icons/linkedin.png" class="img-fluid icon-linked" alt="linkedIn">
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
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
    font-family: 'Montserrat';
    src: url('./src/assets/tipografias/Montserrat/Montserrat-VariableFont_wght.ttf') format('truetype');
}

body {
    font-family: 'Montserrat';
}

  .img-fixed-size {
    width: 200px; 
    height: 200px; 
    object-fit: cover; 
  }
  
  .icon--git {
    width: 4rem;
    margin-right: 2rem;
  }
  
  .icon--linked {
    width: 4rem;
  }

  .card {
    border: none;
  }

  .card-footer {
    background-color: transparent;
  }

  .title-us{
    color: var(--color-verde);
  }
  </style>
  