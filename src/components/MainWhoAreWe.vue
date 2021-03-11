<template>
    <div class="container-fluid">
        <div class="row">
            <div class="bg-color-two col-md-6 nopadding">
                <img class="ml-5 macbook" src="assets/images/book.png" alt="">
            </div>
            <div class="p-5 col-md-6 bg-light">
                <h2 class="mt-3 text-center">Qu'est ce que cela veut dire ?</h2>
                <p class="mt-3 text-center">Aujourd'hui de plus en plus de personnes ont la motivation d'apprendre l'arabe littéraire en immersion totale.Cependant, il n'est pas facile pour tout le monde d'avoir la possibilité de voyager afin de faire des séjours linguistiques. Notre institut est une alternative pour qui désire devenir arabophone. Nous dispensons des cours avec des enseignants expérimentés ayant l'habitude d'enseigner à des non arabophones. Le programme est adapté aux gens n'ayant pas de notions dans la langue arabe. Le plus important est de maîtriser les livres et de finir le programme en sachant parler, écrire et lire avec aisance. Notre équipe a pour but d'encourager et de faciliter à ceux qui le désirent: avancer dans la langue.</p>
                <p class="mt-3 text-center">Que la Paix et la Bénédiction soient sur notre Prophète Muhammad, sa famille et ses compagnons.</p>
                <p class="mb-5 text-center text-muted">Ce site est la propriété exclusive de la société Ibn Maalik immatriculée au répertoire des entreprises, des établissements et des associations sous le numéro 005842118(NINEA).</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'MainWhoAreWe',
    data() {
        return {

        }
    }
}
</script>
<style scoped>
    .container-fluid{
        margin-bottom: 8%;
    }

    .bg-color-two{
        background: linear-gradient(to left, #f8f9fa 30%, #8CD9F1 0%);
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