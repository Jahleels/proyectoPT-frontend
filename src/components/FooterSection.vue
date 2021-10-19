<template>
    <footer>
        <div class="container-footer-all">
        
            <div class="container-body">
        
                <div class="colum1">
                    <h1>Mas informacion de la compañia</h1>
        
                    <p>Somos un equipo de profesionales comprometidos
                        que buscan promover el bienestar y cuidado de la salud mental.</p>
        
                </div>
        
                <div class="colum2">
        
                    <h1>Redes Sociales</h1>
        
                    <div class="column__row">
                        <img src="../assets/iconos/facebook.png">
                        <label>Siguenos en Facebook</label>
                    </div>
                    <div class="column__row">
                        <img src="../assets/iconos/twitter.png">
                        <label>Siguenos en Twitter</label>
                    </div>
                    <div class="column__row">
                        <img src="../assets/iconos/instagram.png">
                        <label>Siguenos en Instagram</label>
                    </div>
                    <div class="column__row">
                        <img src="../assets/iconos/google-plus.png">
                        <label>Siguenos en Google Plus</label>
                    </div>
                    <div class="column__row">
                        <img src="../assets/iconos/pinterest.png">
                        <label>Siguenos en Pinteres</label>
                    </div>
        
        
                </div>
        
                <div class="colum3">
        
                    <h1>Informacion Contactos</h1>
        
                    <div class="row2">
                        <img src="../assets/iconos/house.png">
                        <label>Calle 39 A # 18 - 32
                            Bogotá, Colombia
                        </label>
                    </div>
        
                    <div class="row2">
                        <img src="../assets/iconos/smartphone.png">
                        <label>+(57) 316-549-2695</label>
                        <label> +(57) 318-262-5221</label>
                    </div>
        
                    <div class="row2">
                        <img src="../assets/iconos/contact.png">
                        <label>info@psicotools.com.co</label>
                    </div>
        
                </div>
        
            </div>
        
        </div>
        
        <div class="container-footer">
            <div class="footer">
                <div class="copyright">
                    © Copyright All Rights Reserved | <a href="">Psicotools.</a>
                </div>
        
                <div class="information">
                    <a href="">Informacion Compañia</a> | <a href="">Privacion y Politica</a> | <a href="">Terminos y
                        Condiciones</a>
                </div>
            </div>
        
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterSection'
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

    footer{
    width: 100%;
    background: #f5f8fd;
    color: white;   
    
}

.container-footer-all{
    width: 100%;
    max-width: 1200px;
    margin: auto;
    padding: 40px;
}

.container-body{
    display: flex;
    justify-content: space-between;
}

.colum1{
    max-width: 400px;
}

.colum1 h1{
    font-size: 22px;
}

.colum1 p{
    font-size: 14px;
    color: #C7C7C7;
    margin-top: 20px;
}

.colum2{
    max-width: 400px;
    
}

.colum2 h1{
    font-size: 22px;
}

.column__row{
    margin-top: 20px;
    display: flex;
}

.column__row img{
    width: 36px;
    height: 36px;
}

.column__row label{
    margin-top: 10px;
    margin-left: 20px;
    color: #C7C7C7;
}

.colum3{
    max-width: 400px;
}

.colum3 h1{
    font-size: 22px;
}

.row2{
    margin-top: 20px;
    display: flex;
}

.row2 img{
    width: 36px;
    height: 36px;
}

.row2 label{
    margin-top: 10px;
    margin-left: 20px;
    max-width: 140px;
}

.container-footer{
    width: 100%;  
    background: #f5f8fd;
}

.footer{
    max-width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;  
    padding: 20px;
}

.copyright{
    color: #C7C7C7;
}

.copyright a{
    text-decoration: none;
    color: white;
    font-weight: bold;
}

.information a{
    text-decoration: none;
    color: #C7C7C7;
}

</style>