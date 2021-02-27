<template>
    <div class="container">
        <div class="row">
            <p class="mt-3">Nous vous proposons un programme de cours sérieux et organisés avec des enseignants
                expérimentés, diplômés et ayant l’habitude d’enseigner à des non arabophones.</p>
            <p class="mt-3">Les cours peuvent être donnés de manière collective ou en individuel (cf. tableau
                récapitulatif ci-dessous pour plus de détails). Il vous faudra au préalable un compte Skype pour pouvoir
                y assister.</p>
            <p class="mt-3">Les classes seront par groupe de 3 à 8 élèves et de 3 à 5 élèves pour les moutounes comme
                Alajourroumiyya.</p>
            <p class="mt-3">L’inscription est ouverte en début de session durant une certaine période de temps. Une fois
                le temps impartit arrivé à son terme, les classes seront fermées à l’inscription et il faudra attendre
                la session suivante.</p>
            <p class="mt-3">Les tarifs des différents cours sont indiqués dans le tableau récapitulatif suivant (exemples non exhaustifs):</p>
            <table class="table table-striped">
                <colgroup span="4" class="columns"></colgroup>
                    <tr>
                        <th v-for="thead in theads" v-bind:key="thead.name">{{thead.name}}</th>
                    </tr>
                    <tr>
                        <td v-for="type in types" v-bind:key="type.name">{{type.name}}</td>
                    </tr>
            </table>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'MainClasses',
        data() {
            return {
                theads: [{
                        name: 'Type de cours'
                    },
                    {
                        name: 'Fréquence'
                    },
                    {
                        name: 'Tarifs (pour l\'ensemble de la session'
                    },
                ],
                types: [
                    {name: 'Collectifs'},
                    {name: 'Individuels'},
                    {name: 'Séminaire'}
                ]
            }
        }
    }
</script>
<style scoped>

</style>