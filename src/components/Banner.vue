<template>
<header>
    <div class="bannerbox">
        <img src="image/desert.jpg" class="img-thumbnail" alt="banniere">
        <div class="text">
            <h2>{{title}}</h2>
        </div>
    </div>
</header>
</template>
<script>
export default {
    name: 'Banner',
    data () {
        return {
            title: document.querySelector('a.nav-link.active').innerText
        }
    }
}
</script>
<style scoped>
header{
    height: 100%;
}
.bannerbox{
    /*background: linear-gradient(to bottom, #000, #0001),
    fixed no-repeat center url("~@/assets/images/desert.jpg");
    background-repeat: no-repeat;
    background-size: cover;*/
    position: relative;
    height: 100%;
    width: 100%;
    /*padding: 0;
    margin: 0;*/
}

img{
    /*height: 500px;*/
    width: 100%;
    height: 100%;
    top: 0;
}

.text{
    position: absolute;
    text-align: center;
    top: 40%;
    left: 0;
    right: 0;
}
</style>