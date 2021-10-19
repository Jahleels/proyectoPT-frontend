<template>
    <section class="seccion-nosotros container-lg">
        <div class="row justify-content-center">
            <div class="columna-contenido col-lg-7 col-sm-5 order-1">
        
                <h2 class="columna-contenido__titulo">¿ Quienes somos ?</h2>
        
                <h3 class="columna-contenido__eslogan"><em>Disfruta lo mejor de la psicología profesional en un solo lugar</em></h3>
        
                <p class="columna-contenido__descripcion">
                    Somos un centro de atención psicológica integral que brinda herramientas para la vida y la salud mental de las personas. 
                    Nuestro enfoque integral permite dar cobertura a las diferentes necesidades psicológicas atendiendo, a su vez, 
                    a todos los sectores de la ciudad desde una misma sede, procurando la atención desde la primera infancia hasta la tercera edad. <br><br>
                    Nos caracterizan nuestros valores corporativos:</p>
                <ul class="columna-contenido__lista">
                    <li><i class="bi bi-check2-circle"></i>Trabajo en equipo</li>
                    <li><i class="bi bi-check2-circle"></i>Calidad</li>
                    <li><i class="bi bi-check2-circle"></i>Confianza</li>
                    <li><i class="bi bi-check2-circle"></i>Responsabilidad</li>
                    <li><i class="bi bi-check2-circle"></i>Confidencialidad</li>
                </ul>
        
                <button type="button" class="columna-contenido__btn btn btn-primary">CONOCER MÁS</button>
        
            </div>
        
            <div class="columna-imagen col-lg-5  col-md-6">
                <div class="about-img">
                    <img src="../assets/img/about-img.jpg" class="img-fluid" alt="Persona mirando arquitectura">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'NosotrosSection'
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

    .seccion-nosotros {
    padding: 5rem 0;
}

.columna-contenido__btn,
.header__btn 
{
    padding: 10px 30px;
    font-weight: 600;
    font-size: small;
    letter-spacing: 1.5px;
}
.columna-contenido__lista li i{
    font-size: 18px;
    color: #1bb1dc;
    padding-right: 20px;
}

.columna-contenido__titulo {
    font-weight: 600;
    color: #413e66;
}

.columna-contenido__eslogan {
    color: #413e66;
}

.columna-contenido__descripcion {
    text-align: justify;
}



.about-img::before {
    content: '';
    width: 322px;
    height: 420px;
    background-color: #eaeef5;
    display: block;
    position: absolute;
    left: -30px;
    top:  -30px;
    z-index: -1;
}

.about-img::after {
    content: '';
    width: 322px;
    height: 420px;
    background-color: #eaeef5;
    display: block;
    position: absolute;
    right: -30px;
    bottom: -30px;
    z-index: -1;
}

.about-img > img {
    /* width: 20rem; */
    display: block;
    margin: auto;
    border: solid 8px var(--clr-white);
    border-radius: 4px;
}

.about-img {
    position: relative;
    margin: 30px;
}


</style>