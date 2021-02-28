<template>
    <div class="container">
        <div class="row">
            <form action="" class="mt-5">
                <div class="mb-3">
                    <label for="lastname" class="text-start form-label">Votre nom</label>
                    <input type="text" class="text-start form-control" id="lastname" placeholder="Nom">
                </div>
                <div class="mb-3">
                    <label for="firstname" class="form-label">Votre prénom</label>
                    <input type="text" class="form-control" id="firstname" placeholder="Prénom">
                </div>
                <div class="mb-3">
                    <label for="email" class="form-label">Votre email</label>
                    <input type="email" class="form-control" id="email" placeholder="Email">
                </div>
                <div class="mb-3">
                    <label for="message" class="form-label">Votre message</label>
                    <textarea class="form-control" id="message" rows="3" placeholder="Message"></textarea>
                </div>
                <button type="submit" class="mt-2 mb-3 btn btn-block btn-outline-success">Envoyer</button>
            </form>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>

</style>