<template>
  <div id="nav">
    <nav class="nav justify-content-between">
    
                <img class="nav-logo" src="../assets/img/home/Logo.png" alt="Logo-psicotools">
    
                <ul class="buttons-nav">
                    <li><router-link :to="{ name: 'Home' }"> Inicio</router-link></li>
                    <li><a href="/about">NOSOTROS</a></li>
                    <li><a href="/services">SERVICIOS</a></li>
                    <li><a href="/workshops">TALLERES</a></li>
                    <li><a href="/contact">CONTACTO</a></li>
                    <li><router-link :to="{ name: 'Login' }" v-if="!isLogin"> Login </router-link>
                    <router-link :to="{ name: 'Admin' }" v-else> Admin </router-link></li>
                </ul>
            </nav>
  </div>
</template>

<script>
export default {
  name: "TheNavigation",
  computed: {
    isLogin() {
      return localStorage.getItem("token");
    },
  },
};
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


</style>
