<template>
    <header>

        <div class="container">
            
            <!-- Inicio menú navegación -->
            
            <!-- Fin menú navegación -->
    
    
            <div class="row justify-content-center align-items-center">
                <div class="col-sm-5">
                    <h1 class="header-title">Un equipo de profesionales hecho a tu <span>medida</span></h1>
                    <button type="button" class="btn">conocer más</button>
                </div>
    
                <div class="header-icon col-sm-4">
                    <img src="../assets/img/home/img-1.png">
                </div>
            </div>
        </div>


    </header>
</template>

<script>
export default {
    name: 'HeaderSection'
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

    .nav-logo {
    margin: 10px;
    left: 0;
}

.buttons-nav li {
    display: table-cell;
    padding: 20px;
}
.buttons-nav li a {
    color: #1bb1dc;
    transition: 0.5s; 
    text-decoration: none;
    display: block;
    position: relative;
    color: #413e66;
    padding: 10px 15px;
    transition: 0.3s;
    font-size: 14px;
    font-family: "Banks&Miles", sans-serif;
    text-transform: uppercase;
    font-weight: 600;
}
nav {
    /* float: right; */
    position: relative;
    white-space: nowrap;
    width: 100%;

}

.buttons-nav li:hover>a {
    color: #1bb1dc;
    text-decoration: none;
}

.section-header {
    background-image: url(/img/intro-bg.webp);
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    height: 100vh;
}

.header-title {
    font-weight: 700;
}

.header-title span
{
    color: #1bb1dc;
}
</style>