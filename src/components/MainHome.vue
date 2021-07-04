<template>
    <section class="bg-light">
        <div class="container-fluid">
            <div class="row bg-light">
                <div class="p-5 col-md-6">
                    <h1 class="text-center">بسم الله الرحمن الرحيم</h1>
                    <p class="mt-3 text-center">L'institut Ibn Maalik vous aide à devenir arabophone en suivant des cours de langue arabe en ligne</p>
                    <p class="mt-3 text-center">Apprendre l'arabe en ligne est idéal pour ceux qui n'ont pas la possibilité de voyager.Le programme de l'institut vous permettra d'avancer session par session jusqu'à atteindre un niveau avancé pour la compréhension de la langue ainsi qu'une maîtrise de ses règles de grammaire.Il sera aussi introduit dans le programme des sessions dédiées à l'oral pour maîtriser le parler.</p>
                    <p class="mt-3 text-center">Nous vous proposons un programme structuré avec des enseignants expérimentés d'Égypte habitués à enseigner aux élèves non arabophones.</p>
                    <p class="mt-3 text-center">Nos cours sont ouverts à toutes et à tous sans limite d'âge (hommes, femmes et enfants).</p>
                    <p class="text-start text-center">L'inscription est simple remplissez notre formulaire:<span><a href="#"> cliquez ici</a></span></p>
                </div>
                <div class="bg-color-first col-md-6 nopadding">
                    <img class="macbook" src="assets/images/macbook.jpg" alt="laptop">
                </div>
            </div>
        </div>
    </section>
    <!-- <section class="pt-5 pb-5 bg-light">
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
    </section> -->
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
    .bg-color-first{
        background: linear-gradient(to right, #f8f9fa 30%, #8CD9F1 0%);
        display: flex;
        align-items: center;
    }

    .nopadding {
        padding: 0 !important;
        margin: 0 !important;
    }

    .macbook{
        width: 90%;
        height: auto;
         box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.3);
    }
</style>