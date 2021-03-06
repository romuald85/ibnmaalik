<template>
    <section class="bg-light">
        <div class="container">
            <div class="row bg-light">
                <div class="pt-5 col-md-6">
                    <h1 class="text-center">بسم الله الرحمن الرحيم</h1>
                    <p class="mt-3 text-center">L'institut Ibn Maalik vous aide à devenir arabophone en suivant des cours de langue arabe en ligne</p>
                    <p class="mt-3 text-center">Apprendre l'arabe en ligne est idéal pour ceux qui n'ont pas la possibilité de voyager.Le programme de l'institut vous permettra d'avancer session par session jusqu'à atteindre un niveau avancé pour la compréhension de la langue ainsi qu'une maîtrise de ses règles de grammaire.Il sera aussi introduit dans le programme des sessions dédiées à l'oral pour maîtriser le parler.</p>
                    <p class="mt-3 text-center">Nous vous proposons un programme structuré avec des enseignants expérimentés d'Égypte habitués à enseigner aux élèves non arabophones.</p>
                    <p class="mt-3 text-center">Nos cours sont ouverts à toutes et à tous sans limite d'âge (hommes, femmes et enfants).</p>
                    <p class="text-start text-center">L'inscription est simple remplissez notre formulaire:<span><a href="#"> cliquez ici</a></span></p>
                </div>
                <div class="col-md-6">
                    <img src="assets/images/desert.jpg" class="rounded mx-auto d-block" alt="...">
                    <div class="bg-color">
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="mt-5 mb-5 bg-white">
        <div class="container">
            <p class="ml-3 text-center">Les mérites d'étudier en classe:</p>
            <div class="row">
                <div class="col-md-6">
                    <div class="m-2 card h-50">
                        <div class="card-body">
                            <p>Al mounafasa c'est à dire la concurrence dans le bien.</p>
                        </div>
                    </div>
                    <div class="m-2 card h-50">
                        <div class="card-body">
                            <p>Le dialogue avec les autres élèves.</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="m-2 card h-50">
                        <div class="card-body">
                            <p>L'aide dans les devoirs.</p>
                        </div>
                    </div>
                    <div class="m-2 card h-50">
                        <div class="card-body">
                            <p>Profiter des autres durant le cours là où l'on a des manquements.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section class="pt-5 pb-5 bg-light">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <p>Nos supports sont:</p>
                    <ul>
                        <li>Les quatre tomes de Médine (de débutants à intermédiaires).</li>
                        <li>Alajouroumiyya (pour les plus avancés).</li>
                    </ul>
                </div>
                <div class="col-md-6">
                    <p>Pour toutes questions nous joindre dans la rubrique<span><a href="#"> contact.</a></span></p>
                </div>
            </div>
            <p class="text-center">Que la Paix et la Bénédiction soient sur notre Prophète Muhammad, sa famille et ses compagnons.</p>
        </div>
    </section>
</template>
<script>
import VueAos from 'vue-aos'

export default {
    components: { VueAos },
    name: 'MainHome',
    data() {
        return {

        }
    }
}
</script>
<style scoped>
    .bg-color{
        background-color: #8CD9F1;
        width: 100%;
        height: 100%;
        transform: translateX(45%);
        transform: translateY(-59%);
    }

    img{
        position: relative;
        max-width: 100%;
        height: auto;
        transform: translateY(50%);
        z-index: 100;
    }
</style>