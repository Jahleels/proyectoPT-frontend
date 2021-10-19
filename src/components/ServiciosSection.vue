<template>
    <section id="services" class="seccion-servicios">
            <div class="container">
                <header id="services-header" class="w-50 mx-auto text-center pt-5">
                    <h2>Servicios</h2>
                    <p>
                        Encontrar buenos servicios a la mano no siempre es tan sencillo, sin embargo
                        en <span style="color: #065e77; font-size: large;" >Psicotools</span> nos preocupamos por recibirte con la mejor
                        atención. Conoce mucho más sobre nuestros servicios.
                    </p>
                </header>

                <div class="row">

                    <div class="col-md-6 col-lg-4">
                        <div class="box">
                            <div>
                                <ion-icon name="heart-circle-outline" class="icon heart"></ion-icon>
                                <h4 class="title-box">
                                    <a href="./servicios/acoPsicologico.html">Acompañamiento psicológico</a>
                                </h4>
                            </div>
                            <p class="description text-justify">
                                Es un proceso psicoterapéutico dónde se tiene un espacio de confianza y un
                                acompañamiento empático que permitirá trabajar situaciones ...
                                <a href="./servicios/acoPsicologico.html">Ver más</a>
                            </p>
                        </div>
                    </div>

                    <div class="col-md-6 col-lg-4">
                        <div class="box">
                            <div>
                                <ion-icon name="musical-note" class="icon musical"></ion-icon>
                                <h4 class="title-box"><a href="/services/musica">Musicoterapia</a></h4>
                            </div>
                            <p class="description text-justify">
                                A través de la musicoterapia podrás embarcarte en un camino de autoconocimiento y
                                reconocimiento de tus potenciales, descubriendo ...
                                <a href="/services/musica">Ver más</a>
                            </p>
                        </div>
                    </div>

                    <div class="col-md-6 col-lg-4">
                        <div class="box">
                            <div>
                                <ion-icon name="newspaper-outline" class="icon paper"></ion-icon>
                                <h4 class="title-box">
                                    <a href="./servicios/evaPsicologica.html">Evaluación Psicológica</a>
                                </h4>
                            </div>
                            <p class="description text-justify">
                                Con la evaluación psicológica podrás obtener información respecto a cómo están tus
                                procesos cognitivos, psicológicos o emocionales...
                                <a href="./servicios/evaPsicologica.html">Ver más</a>
                            </p>
                        </div>
                    </div>

                    <div class="col-md-6 col-lg-6">
                        <div class="box">
                            <div>
                                <ion-icon name="glasses-outline" class="icon glasses"></ion-icon>
                                <h4 class="title-box"><a href="/servicios/neuropsicologia.html">Neuropsicología Clínica</a></h4>
                            </div>
                            <p class="description text-justify">
                                Buscamos establecer un perfil global del funcionamiento cognitivo de la
                                persona evaluada mediante diversos instrumentos y herramientas ...
                                <a href="/servicios/neuropsicologia.html">Ver más</a>
                            </p>
                        </div>
                    </div>

                    <div class="col-md-6 col-lg-6">
                        <div class="box">
                            <div>
                                <ion-icon name="game-controller-outline" class="icon controller"></ion-icon>
                                <h4 class="title-box">
                                    <a href="/servicios/acoPsicoeducativo.html">Acompañamiento Psicoeducativo</a>
                                </h4>
                            </div>
                            <p class="description text-justify">
                                Este servicio busca orientar y potenciar el aprendizaje de los estudiantes a través del
                                fortalecimiento de sus estrategias de estudio de acuerdo a sus ...
                                <a href="/servicios/acoPsicoeducativo.html">Ver más</a>
                            </p>
                        </div>
                    </div>
                </div>

            </div>
        </section>
</template>

<script>
export default {
    name: 'ServiciosSection'
}
</script>

<style scoped>
:root {
    /* dark shades of primary color*/
    --clr-primary-1: #065e77;
    --clr-primary-2: #1bb1dc;
    --clr-white: #fff;
    --ff-primary: "Roboto", sans-serif;
    --ff-secondary: "Open Sans", sans-serif;
    --transition: all 0.3s linear;
    --spacing: 0.25rem;
    --radius: 0.5rem;
    --light-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    --dark-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    --max-width: 1170px;
}

/* Global Styles */

*,
::after,
::before {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

@font-face {
    font-family: "Banks&Miles";
    src: url("/fonts/Banks&MilesSingleLine.ttf");
}

body {
    background: var(--clr-white);
    color: #444;
    font-family: "Banks&Miles", sans-serif;
}

ul {
    list-style-type: none;
    padding-left: 0;
}

a {
    color: var(--clr-primary-2);
    transition: 0.5s;
    text-decoration: none;
}

a:hover,
a:active,
a:focus {
    color: #0a98c0;
    outline: none;
    text-decoration: none;
}

p {
    padding: 0;
    margin-bottom: 1.25rem;
}

img:not(.nav-logo) {
    width: 100%;
    display: block;
}

.nav-logo {
    width: 170px;
}

h1,
h2,
h3,
h4,
h5,
h6 {
    font-family: "Banks&Miles", sans-serif;
    font-weight: 400;
    margin-bottom: 0.75rem;
    padding: 0;
}

h1 {
    font-size: 3rem;
}
h2 {
    font-size: 2rem;
}
h3 {
    font-size: 1.25rem;
}
h4 {
    font-size: 0.875rem;
}

.section-center {
    width: 90vw;
    margin: 0 auto;
    max-width: 1170px;
}

    .seccion-servicios {
    background-color: #f5f8fd;
}

.box {
    padding: 30px;
    position: relative;
    overflow: hidden;
    border-radius: 10px;
    margin: 0 10px 40px 10px;
    background: #fff;
    box-shadow: 0 10px 29px 0 rgb(68 88 144 / 10%);
    text-align: center;
}
.icon {
    font-size: 2.5rem; 
    vertical-align: bottom;
    border-radius: 50%;
}
.icon.heart {
    background: #fceef3;
    color: #ff689b;
}

.icon.musical {
    background: #fff0da;
    color: #e98e06;
}

.icon.paper {
    background: #e6fdfc;
    color: #3fcdc7;
}

.icon.glasses {
    background: #eafde7;
    color:#41cf2e;
}

.icon.controller {
    background: #e1eeff;
    color: #2282ff;
}

.title-box {
    padding-top: 10px;
}

.feature-item-aco img{
    height: auto;
    width: auto;
    max-height: 500px;
    max-width: 500px;
    margin-left: 130px;
}

.texto1 {
    text-align: justify;
}


</style>