<template>
    <footer class="bg-dark">
        <div class="row">
            <div class="container d-flex">
                <div class="col-md-6 d-flex flex-column">
                    <a v-bind:href="tab.href" class="mt-2 mb-2" v-for="tab in tabs" v-bind:key="tab.name">{{tab.name}}</a>
                </div>
                <div class="col-md-6 d-flex flex-column">
                    <a href="#" class="mt-2 mb-2" v-for="book in books" v-bind:key="book.title">{{book.title}}</a>
                </div>
            </div>
        </div>
    </footer>
</template>
<script>
export default {
    name: 'Footer',
    data() {
        return {
            tabs: [
                {name: "Qui sommes nous", href: 'who-are-we'},
                {name: "Inscription", href: 'register'},
                {name: "Cours", href: 'classes'},
                {name: "Nous contacter", href: 'contact'},
                {name: 'Conditions générales de vente', href: 'terms'}
            ],
            books: [
                {title: 'Nour al bayan'},
                {title: 'Tomes de Médine'},
                {title: 'Aljouroumiyya'},
                {title: 'Tajwid'},
            ]
        }
    }
}
</script>
<style scoped>

</style>