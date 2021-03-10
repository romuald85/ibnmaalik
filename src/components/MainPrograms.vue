<template>
    <section class="mt-5 bg-white">
        <div class="container">
            <div class="row">
                <div class="mt-4 col-md-4">
                    <h2 class="our-programs">Nos programmes</h2>
                </div>
                <div class="mt-4 row-flex col-md-8">
                    <div class="m-1 card-group">
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>Cours d'arabe</p></a>
                                <a href="register"><p>Cours de Coran</p></a>
                                <a href="register"><p>Cours de tajwid</p></a>
                            </div>
                        </div>
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>La durée d'une session est de 4 semaines</p></a>
                            </div>
                        </div>
                    </div>
                    <div class="m-1 card-group">
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>Cours individuel</p></a>
                                <a href="register"><p>Une seule personne</p></a>
                                <a href="register"><p>5 € / h</p></a>
                            </div>
                        </div>
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>Cours en groupe</p></a>
                                <a href="register"><p>3 personnes minimum</p></a>
                                <a href="register"><p>4 € / h</p></a>
                            </div>
                        </div>
                    </div>
                    <div class="m-1 card-group">
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>Séminaire</p></a>
                                <a href="register"><p>3 personnes minimum</p></a>
                                <a href="register"><p>5 jours / semaine</p></a>
                                <a href="register"><p>Pendant 6 semaines</p></a>
                                <a href="register"><p>80 €</p></a>
                            </div>
                        </div>
                        <div class="m-3 card">
                            <div class="card-body">
                                <a href="register"><p>Le matériel requis:</p></a>
                                <a href="register"><p>Un ordinateur, une tablette ou un smartphone</p></a>
                                <a href="register"><p>Un casque avec micro</p></a>
                                <a href="register"><p>Un compte Zoom ou Whereby</p></a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
    export default {
        name: 'MainPrograms',
        data() {
            return {

            }
        }
    }
</script>
<style scoped>
    .card {
        background-image: linear-gradient(to top, lightgrey 0%, lightgrey 1%, #e0e0e0 26%, #efefef 48%, #d9d9d9 75%, #bcbcbc 100%);
    }

    /* .card-body {
        display: flex;
        flex-flow: column;
    } */

    p {
        text-align: center;
        font-weight: bold;
        margin: auto;
    }

    a{
        text-decoration: none;
        color: #2c3e50;
    }

    div.card{
        transition: transform 0.5s;
    }

    div.card:hover{
        transform: scale(1.1);
    }

    /* .row-flex{
        display: grid;
        grid-template-columns: 50% 50%;
        grid-column-gap: 20px;
        grid-row-gap: 20px;
    } */

    .our-programs:after{
        content: '';
        display: block;
        width: 60%;
        height: 3px;
        background: #8CD9F1;
        margin-top: 10px;
    }
</style>