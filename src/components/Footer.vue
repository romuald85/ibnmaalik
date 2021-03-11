<template>
        <div class="pt-5 pb-3 container-fluid footer">
            <div class="row">
                <div class="col-md-4 d-flex flex-column text-center">
                    <a v-bind:href="tab.href" class="mt-2 mb-2" v-for="tab in tabs" v-bind:key="tab.name">{{tab.name}}</a>
                </div>
                <div class="col-md-4">
                    <p class="pt-3 text-center title">Ibn Maalik | ابن مالك</p>
                </div>
                <div class="col-md-4 d-flex flex-column text-center">
                    <a href="#" class="mt-2 mb-2" v-for="book in books" v-bind:key="book.title">{{book.title}}</a>
                </div>
            </div>
            <p class="copyright text-muted text-center">Copyright 2021 IbnMaalik Tous droits réservés</p>
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
    .footer {
        background: #8CD9F1;
        width: 100%;
        bottom: 0;
        left: 0;
        /* position: fixed;
        z-index: 0; */
    }

    a{
        text-decoration: none;
        font-size: 15px;
        color: #2c3e50;
    }

    .title{
        font-size: 30px;
    }

    .copyright{
        font-size: 13px;
    }
</style>