<template>
    <div class="container">
        <div class="row">
            <div class="mt-5 col-md-4">
                <h2 class="our-books">Nos supports</h2>
            </div>
            <div class="mt-5 row-flex col-md-8">
                <div class="m-1 card-group">
                    <div class="m-3 card">
                        <div class="card-body">
                            <a href="classes">
                                <img src="assets/images/nour1.jpg" alt="">
                            </a>
                        </div>
                        <h5 class="card-title">Nour al bayan</h5>
                    </div>
                    <div class="m-3 card">
                        <div class="card-body">
                            <a href="classes">
                                <img src="assets/images/medine.jpg" alt="">
                            </a>
                        </div>
                        <h5 class="card-title">Les tomes de Médine</h5>
                    </div>
                </div>
                <div class="m-1 card-group">
                    <div class="m-3 card">
                        <div class="card-body">
                            <a href="classes">
                                <img src="assets/images/alajour.jpg" alt="">
                            </a>
                        </div>
                        <h5 class="card-title">Al ajouroumiyya</h5>
                    </div>
                    <div class="m-3 card">
                        <div class="card-body">
                            <a href="classes">
                                <img src="assets/images/tajwid1.jpg" alt="">
                            </a>
                        </div>
                        <h5 class="card-title">Tuhfa al atfal</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'MainBooks',
        data() {
            return {

            }
        }
    }
</script>
<style scoped>
    h2:after{
        content: '';
        width: 40%;
        height: 3px;
        background: #8CD9F1;
        display: block;
        margin-top: 10px;
    }

    /* .row-flex{
        display: grid;
        grid-template-columns: 50% 50%;
        grid-row-gap: 20px;
        grid-column-gap: 20px;
    } */

    .card{
        overflow: hidden;
    }

    .card-body{
        padding: 0;
    }

    img{
        height: 25vw;
        width: 100%;
        transition: transform 2s;
        object-fit: cover;
    }

    img:hover{
        transform: scale(1.1);
    }

    @media screen and (max-width: 585px) {
        img{
        height: 60vw;
        }
    }
</style>