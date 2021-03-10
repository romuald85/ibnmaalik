<template>
    <div class="cont">
        <div class="pt-5 pb-3 container-fluid">
            <div class="row">
                <div class="col-md-4 d-flex flex-column text-center">
                    <a v-bind:href="tab.href" class="mt-2 mb-2" v-for="tab in tabs" v-bind:key="tab.name">{{tab.name}}</a>
                </div>
                <div class="col-md-4">
                    <p class="text-center">Ibn Maalik | ابن مالك</p>
                </div>
                <div class="col-md-4 d-flex flex-column text-center">
                    <a href="#" class="mt-2 mb-2" v-for="book in books" v-bind:key="book.title">{{book.title}}</a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'Footer',
        data() {
            return {
                tabs: [{
                        name: "Qui sommes nous",
                        href: 'who-are-we'
                    },
                    {
                        name: "Inscription",
                        href: 'register'
                    },
                    {
                        name: "Cours",
                        href: 'classes'
                    },
                    {
                        name: "Nous contacter",
                        href: 'contact'
                    },
                    {
                        name: 'Conditions générales de vente',
                        href: 'terms'
                    }
                ],
                books: [{
                        title: 'Nour al bayan'
                    },
                    {
                        title: 'Tomes de Médine'
                    },
                    {
                        title: 'Aljouroumiyya'
                    },
                    {
                        title: 'Tajwid'
                    },
                ]
            }
        }
    }
</script>
<style scoped>
    .cont{
        height: 300px;
    }

    .container-fluid {
        background: #8CD9F1;
        bottom: 0;
        left: 0;
        position: fixed;
        z-index: 999;
    }
</style>