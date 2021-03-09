<template>
    <div class="row">
        <div class="container-fluid">
            <div class="bg-image">

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
        url('/assets/images/desert.jpg') fixed;
        background-repeat: no-repeat;
        background-size: cover;
        height: 300px;
    }
</style>