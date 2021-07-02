<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <form action="" class="mt-5 mb-5" v-on:submit.prevent="checkForm">
                    <div class="row">
                        <p v-if="errors.length">
                            <b>Veuillez corriger l'(les) erreur(s) suivante:</b>
                            <ul>
                                <li style="color: red;" v-for="error in errors" v-bind:key="error">{{error}}</li>
                            </ul>
                        </p>
                        <div class="col-md-6">
                            <div class="mb-3">
                                <label for="lastname" class="text-start form-label">Votre nom</label>
                                <input type="text" v-model="lastname" class="text-start form-control" id="lastname" placeholder="Nom" v-bind:class="errors.lastname ? 'is-invalid' : ''">
                                <p v-bind:key="errors.lastname" class="invalid-feedback">{{errors.lastname}}</p>
                            </div>
                        </div>
                        <div class="col-md-6">
                            <div class="mb-3">
                                <label for="firstname" class="form-label">Votre prénom</label>
                                <input type="text" v-model="firstname" class="form-control" id="firstname" placeholder="Prénom" v-bind:class="errors.firstname ? 'is-invalid' : ''">
                                <p v-bind:key="errors.firstname" class="invalid-feedback">{{errors.firstname}}</p>
                            </div>
                        </div>
                    </div>
                    <div class="row">
                        <div class="mb-3">
                            <label for="email" class="form-label">Votre email</label>
                            <input type="email" v-model="email" class="form-control" id="email" placeholder="Email" v-bind:class="errors.email ? 'is-invalid' : ''">
                            <p v-bind:key="errors.email" class="invalid-feedback">{{errors.email}}</p>
                        </div>
                    </div>
                    <div class="mb-3">
                        <label for="message" class="form-label">Votre message</label>
                        <textarea class="form-control" v-model="message" id="message" rows="3" placeholder="Message" v-bind:class="errors.message ? 'is-invalid' : ''"></textarea>
                        <p v-bind:key="errors.message" class="invalid-feedback">{{errors.message}}</p>
                    </div>
                    <button type="submit" class="mt-5 mb-3 btn btn-block">Envoyer</button>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            errors: [],
            lastname: '',
            firstname: '',
            email: '',
            message: ''
        }
    },
    methods: {
        checkForm: function (e) {
            e.preventDefault()

            let currentObject = this
            axios.post('https://localhost:8000/api/contacts', {
                lastname: this.lastname,
                firstname: this.firstname,
                email: this.email,
                phone: this.phone,
                message: this.message,
            })
            .then((response) => {
                console.log(response.data)
                currentObject.output = response.data
            })
            .catch((error) => {
                    currentObject.output = error
                    if(error.response.data.violations){
                        const apiErrors = {};
                        error.response.data.violations.forEach(violation => {
                            apiErrors[violation.propertyPath] = violation.message
                        })
                        this.errors = apiErrors;
                    }
            })

            if(this.lastname && this.firstname && this.email && this.phone && this.message){
                return true
            }

            this.errors = []

            /*if(!this.lastname){
                this.errors.push('Le champs nom est requis !')
            }
            if(!this.firstname){
                this.errors.push('Le champs prénom est requis !')
            }
            if(!this.email){
                this.errors.push('Le champs email est requis !')
            }
            if(!this.phone){
                this.errors.push('Le champs téléphone est requis !')
            }
            if(!this.message){
                this.errors.push('Le champs message est requis !')
            }*/
        }
    }
}
</script>
<style scoped>
    button{
        background: #8CD9F1;
        color: #2c3e50;
    }
</style>