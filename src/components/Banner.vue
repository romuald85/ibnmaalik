<template>
<div class="bannerbox">
    <img src="image/img1.jpg" class="img-thumbnail" alt="...">
    <div class="text">
        <h2>Institut de langue arabe en ligne</h2>
    </div>
</div>
</template>
<script>
export default {
    name: 'Banner',
    data () {
        return {
            
        }
    }
}
</script>
<style scoped>
.bannerbox{
    position: relative;
    width: 100%;
    padding: 0;
    margin: 0;
}

img{
    height: 500px;
    width: 100%;
}

.text{
    position: absolute;
    text-align: center;
    top: 40%;
    left: 0;
    right: 0;
}
</style>