<template>
    <section class="mt-5 mb-5 bg-white">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <h2 class="our-programs">Nos programmes</h2>
                </div>
                <div class="row-flex col-md-8">
                    <div class="card">
                        <div class="card-body">
                            <p>Cours d'arabe</p>
                            <p>Cours de Coran</p>
                            <p>Cours de tajwid</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-body">
                            <p>La durée d'une session est de 4 semaines</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-body">
                            <p>Cours individuel</p>
                            <p>Une seule personne</p>
                            <p>5 € / h</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-body">
                            <p>Cours en groupe</p>
                            <p>3 personnes minimum</p>
                            <p>4 € / h</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-body">
                            <p>Séminaire</p>
                            <p>3 personnes minimum</p>
                            <p>5 jours / semaine</p>
                            <p>Pendant 6 semaines</p>
                            <p>80 €</p>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-body">
                            <p>Le matériel requis:</p>
                            <p>Un ordinateur, une tablette ou un smartphone</p>
                            <p>Un casque avec micro</p>
                            <p>Un compte Zoom ou Whereby</p>
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

    .card-body {
        display: flex;
        flex-flow: column;
    }

    p {
        text-align: center;
        margin: auto;
    }

    .row-flex{
        display: grid;
        grid-template-columns: 50% 50%;
        grid-column-gap: 20px;
        grid-row-gap: 20px;
    }

    .our-programs:after{
        content: '';
        display: block;
        width: 60%;
        height: 3px;
        background: #8CD9F1;
        margin-top: 10px;
    }
</style>