<template>
    <div class="container-fluid">
        <div class="row bg-image">
            <div class="cont-text-button">
                <h3 class="pb-4 text-dark">Vous avez une question ? N'hésitez pas à nous contacter</h3>
                <a type="button" href="#contact" class="btn btn-outline-dark btn-lg">Contact</a>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'MainBackground',
    data() {
        return {

        }
    }
}
</script>
<style scoped>
    .bg-image{
        background: linear-gradient(to bottom, #B6E3F1, #0001), 
        url('/assets/images/landscape.jpg') fixed;
        background-repeat: no-repeat;
        background-size: cover;
        height: 300px;
        display: flex;
    }

    .cont-text-button{
       text-align: center;
       margin: auto;
    }
</style>