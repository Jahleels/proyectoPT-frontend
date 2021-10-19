<template>
    <section class="section-workshops">

            <article class="container-card-workshop container-card-workshop--margin">
                <a href="/views/emocionaditos.html" class="link-workshop">
                    <h3 class="link-workshop__title">Emocionaditos</h3>
                </a>
                <figure class="container-logo-workshop">
                    <img src="../assets/img/icons/emocional.webp" alt="" class="container-logo-workshop__img" loading="lazy">
                </figure>
                <p class="container-paragraph-workshop">
                    El desarrollo emocional es un proceso difícil que requiere de tiempo y acompañamiento de los
                    cuidadores para que se dé de una manera adecuada. El saber manejar las emociones ...
                    <a href="../assets/views/emocionaditos.html" class="container-paragraph-workshop__link">Ver más</a>
                </p>
            </article>

            <article class="container-card-workshop">
                <a href="views/aprendeConmigo.html" class="link-workshop">
                    <h3 class="link-workshop__title">Aprende Conmigo</h3>
                </a>
                <figure class="container-logo-workshop">
                    <img src="../assets/img/icons/reading.webp" alt="" class="container-logo-workshop__img" loading="lazy">
                </figure>
                <p class="container-paragraph-workshop">
                    Es común que nuestros hijos desde muy pequeñitos presenten algunas dificultades para desenvolverse
                    con facilidad en el colegio; por ejemplo, algunas veces no atienden a las ...
                    <a href="views/aprendeConmigo.html" class="container-paragraph-workshop__link">Ver más</a>
                </p>
            </article>

            <article class="container-card-workshop">
                <a href="../assets/views/levelUp.html" class="link-workshop">
                    <h3 class="link-workshop__title">LEVEL UP!</h3>
                </a>
                <figure class="container-logo-workshop">
                    <img src="../assets/img/icons/games.webp" alt="" class="container-logo-workshop__img" loading="lazy">
                </figure>
                <p class="container-paragraph-workshop">
                    En Psicotools sabemos que los videojuegos han influenciado a niños, adolescentes y jóvenes que los
                    utilizan como medio para divertirse, relacionarse y aprender. Sin embargo ...
                    <a href="../assets/views/levelUp.html" class="container-paragraph-workshop__link">Ver más</a>
                </p>
            </article>

            <article class="container-card-workshop container-card-workshop4">
                <a href="../assets/views/embarazo.html" class="link-workshop">
                    <h3 class="link-workshop__title">El embarazo, una aventura para renacer</h3>
                </a>
                <figure class="container-logo-workshop">
                    <img src="../assets/img/icons/heart.webp" alt="" class="container-logo-workshop__img" loading="lazy">
                </figure>
                <p class="container-paragraph-workshop">
                    ¿Sabías qué la forma cómo vives tu embarazo y las experiencias que tienes influyen en la
                    personalidad de tu bebé y en su forma de ser como adulto? Con base en la psicología peri y
                    prenatal...
                    <a href="views/embarazo.html" class="container-paragraph-workshop__link">Ver más</a>
                </p>
            </article>

            <article class="container-card-workshop container-card-workshop5">
                <a href="views/pharmakon.html" class="link-workshop">
                    <h3 class="link-workshop__title">PHÁRMAKON</h3>
                </a>
                <figure class="container-logo-workshop">
                    <img src="../assets/img/icons/humano.webp" alt="" class="container-logo-workshop__img" loading="lazy">
                </figure>
                <p class="container-paragraph-workshop">
                    Las drogas lícitas e ilícitas, sintéticas y naturales existen y circulan en nuestros entornos
                    cotidianos; las utilizaron, utilizan o utilizarán personas cercanas a nosotros, y es muy probable
                    que en algún ...
                    <a href="views/pharmakon.html" class="container-paragraph-workshop__link">Ver más</a>
                </p>
            </article>
        </section>
</template>

<script>
export default {
    name: 'TalleresSection'
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

    .section-workshops{
    display: grid;
    grid-template-rows: repeat(5, 420px);
    background-color: #edf3ff;
    padding-top: 6rem;
    position: relative;
}
.title-workshop{
    color: #413E66;
    font-size: 34px;
    font-weight: 600;
}
.container-card-workshop{
    width: 88%;
    display: grid;
    grid-template-rows: 3fr 3fr 7fr;
    margin: 0 auto 40px auto;
    border-radius: var(--radius);
    background-color: white;
    padding: 30px;
    text-align: center;
    box-shadow: var(--light-shadow);
}
.link-workshop{
    grid-row: 2;
    align-self: center;
}
.container-logo-workshop{
    width: 3.5rem;
    grid-row: 1;
    margin: 0;
    justify-self: center;
}
.link-workshop{
    color: black;
}
.link-workshop__title{
    font-weight: 700;
    font-size: 1rem;
    margin: 0 0 0 0;
}
.container-paragraph-workshop{
    text-align: justify;
    margin: 0;
    line-height: 1.4rem;
    font-size: .8rem;
    color: #444444;
}
.container-paragraph-workshop__link{
    color: var(--clr-primary-2);
}

.container-section-emocionaditos, .container-section-aprendeConmigo, .container-section-levelUp, .container-section-embarazo, .container-section-pharmakon{
    padding: 1.3rem;
}
.container-figure-emocionaditos, .container-figure-aprendeConmigo, .container-figure-levelUp, .container-figure-embarazo, .container-figure-pharmakon{
    width: 75vw;
    margin-top: 4rem;
    margin-bottom: 7rem;
    margin-left: auto;
    margin-right: auto;
}
.container-figure-emocionaditos__img, .container-figure-aprendeConmigo__img, .container-figure-levelUp__img,.container-figure-embarazo__img, .container-figure-pharmakon__img{
    border-radius: .8rem;
}
.container-info-emocionaditos__title, .container-info-aprendeConmigo__title, .container-info-levelUp__title,.container-info-embarazo__title, .container-info-pharmakon__title{
    font-weight: 700;
    font-size: 1.1rem;
}
.container-info-emocionaditos__paragraph,.container-info-aprendeConmigo__paragraph, .container-info-levelUp__paragraph, .container-info-embarazo__paragraph, .container-info-pharmakon__paragraph{
    text-align: justify;
}
.container-info-levelUp__span{
    color: var(--clr-primary-2);
}
.button-workshop {
    display: inline-block;
    border: none;
    padding: .7rem;
    font-size: .8rem;
    color: white;
    border-radius: .4rem;
    text-align: center;
    margin-bottom: 2.5rem;
    margin-top: .8rem;
}
.button-workshop--blue {
    width: 7.5rem;
    background-color: var(--clr-primary-2);
}

.button-workshop--red {
    width: 6rem;
    background-color: #DC3545;
}

.container-main{
    padding: .8rem;
}
.container-form{
    border: 1px solid var(--clr-primary-2);
    padding: 1.2rem;
    background-color: white;
    color:rgb(156, 156, 156);
    text-align: center;
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -ms-border-radius: 5px;
    -o-border-radius: 5px;
}
.container-form__title{
    font-size: 1.7rem;
    margin-bottom: 1rem;
    color: var(--clr-primary-2);
    font-weight: 700;
}
.form-workshop-registration__input, .select-workshop-registration{
    display: block;
    width: 100%;
    height: 2.3rem;
    margin-bottom: 1.2rem;
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -ms-border-radius: 5px;
    -o-border-radius: 5px;
    border: 2px solid rgb(219, 219, 219);
    background-color: white;
    padding-left: .7rem;
    color:rgb(129, 129, 129);
}
.form-workshop-registration__btn{
    width: 7rem;
    font-size: .7rem;
    padding: .6rem;
    border: none;
    background-color: var(--clr-primary-2);
    color: white;
    border-radius: 5px;
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    -ms-border-radius: 5px;
    -o-border-radius: 5px;
    margin-bottom: 20px;
}
.form-workshop-registration__input:focus, .select-workshop-registration:focus{
    outline: none;
}
.container-main{
    background-image: url(/img/intro-bg.webp);
    background-size: cover;
    background-repeat: no-repeat;
}
.container-info-form-register {
    padding: .7rem;
    border-bottom: 1px solid gray;
    margin: 3rem 0 1rem 0;
}
.container-info-form-register__paragraph{
    font-weight: 700;
}
.container-info-contact {
    padding: .7rem;
}
.container-list-info{
    padding-left: 0;
}
.container-list-info__item {
    font-weight: 600;
}
.container-telephone__title, .container-address__title, .container-email__title{
    color: var(--clr-primary-2);
    font-weight: 700;
}

.container-list-info__icon{
    margin-right: .2rem;
}

@media screen and (min-width: 630px) {
    .container-section-emocionaditos, .container-section-aprendeConmigo, .container-section-levelUp, .container-section-embarazo, .container-section-pharmakon{
        padding: 3rem;
    }
    .container-figure-emocionaditos, .container-figure-aprendeConmigo, .container-figure-levelUp, .container-figure-embarazo, .container-figure-pharmakon{
        width: 56vw;
    }
    .container-info-emocionaditos__title, .container-info-aprendeConmigo__title, .container-info-levelUp__title,.container-info-embarazo__title, .container-info-pharmakon__title{
        font-size: 1.2rem;
    }

    .container-form{
        width: 60%;
        margin-left: auto;
        margin-right: auto;
    }
}

@media screen and (min-width: 770px) {
    .section-workshops{
        display: grid;
        grid-template-columns: repeat(auto-fill, 350px);
        grid-auto-flow: dense;
        justify-content: center;
    }
    .container-paragraph-workshop{
        font-size: .7rem;
    }
    .link-workshop__title{
        font-size: .9rem;
    }
    .container-section-emocionaditos, .container-section-aprendeConmigo, .container-section-levelUp, .container-section-embarazo, .container-section-pharmakon{
        padding: 5rem;
    }
    .container-figure-emocionaditos, .container-figure-aprendeConmigo, .container-figure-levelUp, .container-figure-embarazo, .container-figure-pharmakon{
        width: 47vw;
    }
    .container-info-emocionaditos__title, .container-info-aprendeConmigo__title, .container-info-levelUp__title,.container-info-embarazo__title, .container-info-pharmakon__title{
        font-size: 1.3rem;
    }
    .container-main{
        display: grid;
        grid-template-columns: 60% 40%;
        padding: 2rem;
        align-content: center;
        justify-content: center;
    }
    .container-form{
        width: 80%;
        height: 82%;
        justify-self: center;
        align-self: center;
    }
}

@media screen and (min-width: 990px) {
    .section-workshops {
        display: grid;
        grid-template-columns: repeat(auto-fit, 300px);
        grid-template-rows: 440px 440px;
        grid-auto-flow: initial;
    }

    .container-section-emocionaditos, .container-section-aprendeConmigo, .container-section-levelUp, .container-section-embarazo, .container-section-pharmakon{
        display: grid;
        grid-template-columns: repeat(2, 50%);
        column-gap: 1rem;
        align-content: flex-start;
        justify-content: center;
    }
    .container-figure-emocionaditos, .container-figure-aprendeConmigo, .container-figure-levelUp, .container-figure-embarazo, .container-figure-pharmakon{
        width: 87%;
        margin: 0;
        justify-self: center;
    }
    .container-info-emocionaditos__paragraph,.container-info-aprendeConmigo__paragraph, .container-info-levelUp__paragraph, .container-info-embarazo__paragraph, .container-info-pharmakon__paragraph{
        grid-column: 2;
    }
    .button-workshop {
        grid-column: 2;
    }
    .container-figure-emocionaditos__img, .container-figure-aprendeConmigo__img, .container-figure-levelUp__img,.container-figure-embarazo__img, .container-figure-pharmakon__img{
        height: 380px;
    }
    .container-form{
        width: 80%;
        height: 85%;
    }
}

@media screen and (min-width: 1200px) {
    .section-workshops {
        height: 900px;
        display: grid;
        grid-template-columns: repeat(3, 390px);
        grid-template-rows: 360px 360px;
        grid-auto-flow: row;
        padding: 0;
        align-content: center;
    }
    .container-card-workshop{
        transform: scale(1);
        transition: transform .8s;
        -webkit-transform: scale(1);
        -moz-transform: scale(1);
        -ms-transform: scale(1);
        -o-transform: scale(1);
        -webkit-transition: transform .8s;
        -moz-transition: transform .8s;
        -ms-transition: transform .8s;
        -o-transition: transform .8s;
}
    .container-card-workshop:hover{
        transform: scale(1.1);
        transition: transform .6s;
        -webkit-transform: scale(1.1);
        -moz-transform: scale(1.1);
        -ms-transform: scale(1.1);
        -o-transform: scale(1.1);
        -webkit-transition: transform .6s;
        -moz-transition: transform .6s;
        -ms-transition: transform .6s;
        -o-transition: transform .6s;
}
    .container-section-emocionaditos, .container-section-aprendeConmigo, .container-section-levelUp, .container-section-embarazo, .container-section-pharmakon{
        grid-template-columns: 30% 37%;
        column-gap: 3rem;
        align-content: center;
    }

    .button-workshop--blue:hover, .form-workshop-registration__btn:hover {
        color:white;
        background-color: #1294b8;
    }
    
    .button-workshop--red:hover {
        color:white;
        background-color: #aa2633;
    }

    .container-main{
        grid-template-columns: 30% 29%;
        column-gap: 2rem;
    }
    .container-form{
        height: 85%;
    }
}
</style>