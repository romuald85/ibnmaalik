<template>
    <section class="bg-white">
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
                                <a href="register"><p>Un compte Zoom</p></a>
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
    section{
        background: linear-gradient(to bottom, #B6E3F1, #0001),
        fixed no-repeat center url("/assets/images/desert2.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
    }
    .card {
       /*background-image: linear-gradient(to right top, #8cd9f1, #84dcf1, #7de0f1, #77e3ef, #71e6ed);*/
       /*background-image: linear-gradient(to right top, #d99661, #b6b26a, #8fc694, #77d3c8, #8cd9f1);*/
       /*background: rgb(140,217,241);
        background: linear-gradient(90deg, rgba(140,217,241,1) 0%, rgba(217,150,97,1) 100%);*/
        /*background: #e3be81;*/
        /*background-image: linear-gradient(to right top, #e3be81, #d8af76, #cd9f6b, #c29161, #b68257);*/
        background: rgba(0, 0, 0, 0.05);
        backdrop-filter: blur(5px);
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