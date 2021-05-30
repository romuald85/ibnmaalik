<template>

    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <p class="mt-5">Pour vous inscrire, c’est très simple il vous suffit de remplir le formulaire en bas de
                    page, après avoir pris connaissance des informations ci-dessous. Le paiement se fera avant chaque
                    session d’une durée de 4 semaines. Les retards et absences des enseignants donneront lieux à des
                    séances
                    de rattrapage. Par contre aucune responsabilité du site ne sera engagée pour tout retard/absence de
                    l’élève. La session et le support sont deux choses différentes c’est à dire que le support est un
                    des
                    tomes de Medine par exemple et la session durera 4 semaines. Ceci n’implique pas que vous finirez le
                    tome en 4 semaines loin de là car cette méthode, comprenant 4 tomes, est enseignée sur deux années
                    complètes dans l’institut de langue de l’université de Medine.</p>
                <p class="mt-3 text-start">Le matériel requis:</p>
                <ul>
                    <li class="text-start" v-for="equipment in equipments" v-bind:key="equipment.name">
                        {{equipment.name}}
                    </li>
                </ul>
            </div>

            <div class="col-md-6">
                <p class="mt-3">Le programme est très souple, vous ne vous engagez avec nous que pour la durée de 4
                    semaines. Vous avez ensuite la possibilité de vous arrêter ou de faire une pause d’une ou plusieurs
                    sessions tout en sachant que l’assiduité est un facteur important dans notre programme. Les cours
                    seront
                    dispensés, selon votre préférence, de manière collective ou individuelle. Concernant les cours
                    collectifs, les classes seront limitées à 8 élèves maximum et 3 minimum et pour les moutounes comme
                    Alajourroumiyya 5 maximum et 3 minimum, ceci afin de garantir la qualité de l’enseignement. La
                    fréquence
                    de ces cours sera de 3 jours par semaine, 2h par jour. Concernant les cours individuels la fréquence
                    des
                    cours sera au choix de 4h ou 6h par semaine. Les tarifs des c ours sont disponibles dans la rubrique
                    Cours d’arabe littéraire. Les cours de tajwid sont de 2 jours par semaine, 1h par jour. Pour une
                    demande
                    d’inscription, vous pouvez remplir le formulaire ci-dessous , nous vous répondrons dans les plus
                    brefs
                    délais.
                </p>
            </div>
        </div>
        <div class="row">
            <div class="col-md-6 mx-auto">
                <form name="register" v-on:submit.prevent="checkForm">
                    <fieldset>
                        <legend>Informations personnelles</legend>
                        <p v-if="errors.length">
                            <b>Veuillez corriger l'(les) erreur(s) suivante: </b>
                            <ul>
                                <li style="color: red;" v-for="error in errors" v-bind:key="error">{{error}}</li>
                            </ul>
                        </p>
                        <div class="row">
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label for="lastname" class="text-start form-label">Votre nom</label>
                                    <input type="text" v-model="lastname" class="input-field text-start form-control"
                                        id="lastname" placeholder="Nom">
                                </div>
                            </div>
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label for="firstname" class="form-label">Votre prénom</label>
                                    <input type="text" v-model="firstname" class="input-field form-control"
                                        id="firstname" placeholder="Prénom">
                                </div>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label for="age" class="form-label">Votre âge</label>
                                    <input type="number" v-model="age" class="input-field form-control" id="age"
                                        placeholder="Âge" min="0">
                                </div>
                            </div>
                            <div class="col-md-6">
                                <div class="mb-3">
                                    <label for="phone" class="form-label">Votre téléphone</label>
                                    <input type="text" v-model="phone" class="input-field form-control" id="phone"
                                        placeholder="Téléphone">
                                </div>
                            </div>
                        </div>
                        <div class="row">
                            <div class="mb-3">
                                <label for="email" class="form-label">Votre email</label>
                                <input type="email" v-model="email" class="input-field form-control" id="email"
                                    placeholder="Email">
                            </div>
                            <!-- <div class="col-md-6">
                                <div class="mb-3">
                                    <label for="verifemail" class="form-label">Vérification email</label>
                                    <input type="email" v-model="verifemail" class="input-field form-control"
                                        id="verifemail" placeholder="Vérification email">
                                </div>
                            </div> -->
                        </div>
                        <div class="mb-3">
                            <label for="country" class="form-label">Votre pays</label>
                            <select id="country" name="country" class="form-control" v-model="country">
                                <option value="Afghanistan">Afghanistan</option>
                                <option value="Åland Islands">Åland Islands</option>
                                <option value="Albania">Albania</option>
                                <option value="Algeria">Algeria</option>
                                <option value="American Samoa">American Samoa</option>
                                <option value="Andorra">Andorra</option>
                                <option value="Angola">Angola</option>
                                <option value="Anguilla">Anguilla</option>
                                <option value="Antarctica">Antarctica</option>
                                <option value="Antigua and Barbuda">Antigua and Barbuda</option>
                                <option value="Argentina">Argentina</option>
                                <option value="Armenia">Armenia</option>
                                <option value="Aruba">Aruba</option>
                                <option value="Australia">Australia</option>
                                <option value="Austria">Austria</option>
                                <option value="Azerbaijan">Azerbaijan</option>
                                <option value="Bahamas">Bahamas</option>
                                <option value="Bahrain">Bahrain</option>
                                <option value="Bangladesh">Bangladesh</option>
                                <option value="Barbados">Barbados</option>
                                <option value="Belarus">Belarus</option>
                                <option value="Belgium">Belgium</option>
                                <option value="Belize">Belize</option>
                                <option value="Benin">Benin</option>
                                <option value="Bermuda">Bermuda</option>
                                <option value="Bhutan">Bhutan</option>
                                <option value="Bolivia">Bolivia</option>
                                <option value="Bosnia and Herzegovina">Bosnia and Herzegovina</option>
                                <option value="Botswana">Botswana</option>
                                <option value="Bouvet Island">Bouvet Island</option>
                                <option value="Brazil">Brazil</option>
                                <option value="British Indian Ocean Territory">British Indian Ocean Territory</option>
                                <option value="Brunei Darussalam">Brunei Darussalam</option>
                                <option value="Bulgaria">Bulgaria</option>
                                <option value="Burkina Faso">Burkina Faso</option>
                                <option value="Burundi">Burundi</option>
                                <option value="Cambodia">Cambodia</option>
                                <option value="Cameroon">Cameroon</option>
                                <option value="Canada">Canada</option>
                                <option value="Cape Verde">Cape Verde</option>
                                <option value="Cayman Islands">Cayman Islands</option>
                                <option value="Central African Republic">Central African Republic</option>
                                <option value="Chad">Chad</option>
                                <option value="Chile">Chile</option>
                                <option value="China">China</option>
                                <option value="Christmas Island">Christmas Island</option>
                                <option value="Cocos (Keeling) Islands">Cocos (Keeling) Islands</option>
                                <option value="Colombia">Colombia</option>
                                <option value="Comoros">Comoros</option>
                                <option value="Congo">Congo</option>
                                <option value="Congo, The Democratic Republic of The">Congo, The Democratic Republic of
                                    The
                                </option>
                                <option value="Cook Islands">Cook Islands</option>
                                <option value="Costa Rica">Costa Rica</option>
                                <option value="Cote D'ivoire">Cote D'ivoire</option>
                                <option value="Croatia">Croatia</option>
                                <option value="Cuba">Cuba</option>
                                <option value="Cyprus">Cyprus</option>
                                <option value="Czech Republic">Czech Republic</option>
                                <option value="Denmark">Denmark</option>
                                <option value="Djibouti">Djibouti</option>
                                <option value="Dominica">Dominica</option>
                                <option value="Dominican Republic">Dominican Republic</option>
                                <option value="Ecuador">Ecuador</option>
                                <option value="Egypt">Egypt</option>
                                <option value="El Salvador">El Salvador</option>
                                <option value="Equatorial Guinea">Equatorial Guinea</option>
                                <option value="Eritrea">Eritrea</option>
                                <option value="Estonia">Estonia</option>
                                <option value="Ethiopia">Ethiopia</option>
                                <option value="Falkland Islands (Malvinas)">Falkland Islands (Malvinas)</option>
                                <option value="Faroe Islands">Faroe Islands</option>
                                <option value="Fiji">Fiji</option>
                                <option value="Finland">Finland</option>
                                <option value="France" selected>France</option>
                                <option value="French Guiana">French Guiana</option>
                                <option value="French Polynesia">French Polynesia</option>
                                <option value="French Southern Territories">French Southern Territories</option>
                                <option value="Gabon">Gabon</option>
                                <option value="Gambia">Gambia</option>
                                <option value="Georgia">Georgia</option>
                                <option value="Germany">Germany</option>
                                <option value="Ghana">Ghana</option>
                                <option value="Gibraltar">Gibraltar</option>
                                <option value="Greece">Greece</option>
                                <option value="Greenland">Greenland</option>
                                <option value="Grenada">Grenada</option>
                                <option value="Guadeloupe">Guadeloupe</option>
                                <option value="Guam">Guam</option>
                                <option value="Guatemala">Guatemala</option>
                                <option value="Guernsey">Guernsey</option>
                                <option value="Guinea">Guinea</option>
                                <option value="Guinea-bissau">Guinea-bissau</option>
                                <option value="Guyana">Guyana</option>
                                <option value="Haiti">Haiti</option>
                                <option value="Heard Island and Mcdonald Islands">Heard Island and Mcdonald Islands
                                </option>
                                <option value="Holy See (Vatican City State)">Holy See (Vatican City State)</option>
                                <option value="Honduras">Honduras</option>
                                <option value="Hong Kong">Hong Kong</option>
                                <option value="Hungary">Hungary</option>
                                <option value="Iceland">Iceland</option>
                                <option value="India">India</option>
                                <option value="Indonesia">Indonesia</option>
                                <option value="Iran, Islamic Republic of">Iran, Islamic Republic of</option>
                                <option value="Iraq">Iraq</option>
                                <option value="Ireland">Ireland</option>
                                <option value="Isle of Man">Isle of Man</option>
                                <option value="Israel">Israel</option>
                                <option value="Italy">Italy</option>
                                <option value="Jamaica">Jamaica</option>
                                <option value="Japan">Japan</option>
                                <option value="Jersey">Jersey</option>
                                <option value="Jordan">Jordan</option>
                                <option value="Kazakhstan">Kazakhstan</option>
                                <option value="Kenya">Kenya</option>
                                <option value="Kiribati">Kiribati</option>
                                <option value="Korea, Democratic People's Republic of">Korea, Democratic People's
                                    Republic
                                    of
                                </option>
                                <option value="Korea, Republic of">Korea, Republic of</option>
                                <option value="Kuwait">Kuwait</option>
                                <option value="Kyrgyzstan">Kyrgyzstan</option>
                                <option value="Lao People's Democratic Republic">Lao People's Democratic Republic
                                </option>
                                <option value="Latvia">Latvia</option>
                                <option value="Lebanon">Lebanon</option>
                                <option value="Lesotho">Lesotho</option>
                                <option value="Liberia">Liberia</option>
                                <option value="Libyan Arab Jamahiriya">Libyan Arab Jamahiriya</option>
                                <option value="Liechtenstein">Liechtenstein</option>
                                <option value="Lithuania">Lithuania</option>
                                <option value="Luxembourg">Luxembourg</option>
                                <option value="Macao">Macao</option>
                                <option value="Macedonia, The Former Yugoslav Republic of">Macedonia, The Former
                                    Yugoslav
                                    Republic of</option>
                                <option value="Madagascar">Madagascar</option>
                                <option value="Malawi">Malawi</option>
                                <option value="Malaysia">Malaysia</option>
                                <option value="Maldives">Maldives</option>
                                <option value="Mali">Mali</option>
                                <option value="Malta">Malta</option>
                                <option value="Marshall Islands">Marshall Islands</option>
                                <option value="Martinique">Martinique</option>
                                <option value="Mauritania">Mauritania</option>
                                <option value="Mauritius">Mauritius</option>
                                <option value="Mayotte">Mayotte</option>
                                <option value="Mexico">Mexico</option>
                                <option value="Micronesia, Federated States of">Micronesia, Federated States of</option>
                                <option value="Moldova, Republic of">Moldova, Republic of</option>
                                <option value="Monaco">Monaco</option>
                                <option value="Mongolia">Mongolia</option>
                                <option value="Montenegro">Montenegro</option>
                                <option value="Montserrat">Montserrat</option>
                                <option value="Morocco">Morocco</option>
                                <option value="Mozambique">Mozambique</option>
                                <option value="Myanmar">Myanmar</option>
                                <option value="Namibia">Namibia</option>
                                <option value="Nauru">Nauru</option>
                                <option value="Nepal">Nepal</option>
                                <option value="Netherlands">Netherlands</option>
                                <option value="Netherlands Antilles">Netherlands Antilles</option>
                                <option value="New Caledonia">New Caledonia</option>
                                <option value="New Zealand">New Zealand</option>
                                <option value="Nicaragua">Nicaragua</option>
                                <option value="Niger">Niger</option>
                                <option value="Nigeria">Nigeria</option>
                                <option value="Niue">Niue</option>
                                <option value="Norfolk Island">Norfolk Island</option>
                                <option value="Northern Mariana Islands">Northern Mariana Islands</option>
                                <option value="Norway">Norway</option>
                                <option value="Oman">Oman</option>
                                <option value="Pakistan">Pakistan</option>
                                <option value="Palau">Palau</option>
                                <option value="Palestinian Territory, Occupied">Palestinian Territory, Occupied</option>
                                <option value="Panama">Panama</option>
                                <option value="Papua New Guinea">Papua New Guinea</option>
                                <option value="Paraguay">Paraguay</option>
                                <option value="Peru">Peru</option>
                                <option value="Philippines">Philippines</option>
                                <option value="Pitcairn">Pitcairn</option>
                                <option value="Poland">Poland</option>
                                <option value="Portugal">Portugal</option>
                                <option value="Puerto Rico">Puerto Rico</option>
                                <option value="Qatar">Qatar</option>
                                <option value="Reunion">Reunion</option>
                                <option value="Romania">Romania</option>
                                <option value="Russian Federation">Russian Federation</option>
                                <option value="Rwanda">Rwanda</option>
                                <option value="Saint Helena">Saint Helena</option>
                                <option value="Saint Kitts and Nevis">Saint Kitts and Nevis</option>
                                <option value="Saint Lucia">Saint Lucia</option>
                                <option value="Saint Pierre and Miquelon">Saint Pierre and Miquelon</option>
                                <option value="Saint Vincent and The Grenadines">Saint Vincent and The Grenadines
                                </option>
                                <option value="Samoa">Samoa</option>
                                <option value="San Marino">San Marino</option>
                                <option value="Sao Tome and Principe">Sao Tome and Principe</option>
                                <option value="Saudi Arabia">Saudi Arabia</option>
                                <option value="Senegal">Senegal</option>
                                <option value="Serbia">Serbia</option>
                                <option value="Seychelles">Seychelles</option>
                                <option value="Sierra Leone">Sierra Leone</option>
                                <option value="Singapore">Singapore</option>
                                <option value="Slovakia">Slovakia</option>
                                <option value="Slovenia">Slovenia</option>
                                <option value="Solomon Islands">Solomon Islands</option>
                                <option value="Somalia">Somalia</option>
                                <option value="South Africa">South Africa</option>
                                <option value="South Georgia and The South Sandwich Islands">South Georgia and The South
                                    Sandwich Islands</option>
                                <option value="Spain">Spain</option>
                                <option value="Sri Lanka">Sri Lanka</option>
                                <option value="Sudan">Sudan</option>
                                <option value="Suriname">Suriname</option>
                                <option value="Svalbard and Jan Mayen">Svalbard and Jan Mayen</option>
                                <option value="Swaziland">Swaziland</option>
                                <option value="Sweden">Sweden</option>
                                <option value="Switzerland">Switzerland</option>
                                <option value="Syrian Arab Republic">Syrian Arab Republic</option>
                                <option value="Taiwan, Province of China">Taiwan, Province of China</option>
                                <option value="Tajikistan">Tajikistan</option>
                                <option value="Tanzania, United Republic of">Tanzania, United Republic of</option>
                                <option value="Thailand">Thailand</option>
                                <option value="Timor-leste">Timor-leste</option>
                                <option value="Togo">Togo</option>
                                <option value="Tokelau">Tokelau</option>
                                <option value="Tonga">Tonga</option>
                                <option value="Trinidad and Tobago">Trinidad and Tobago</option>
                                <option value="Tunisia">Tunisia</option>
                                <option value="Turkey">Turkey</option>
                                <option value="Turkmenistan">Turkmenistan</option>
                                <option value="Turks and Caicos Islands">Turks and Caicos Islands</option>
                                <option value="Tuvalu">Tuvalu</option>
                                <option value="Uganda">Uganda</option>
                                <option value="Ukraine">Ukraine</option>
                                <option value="United Arab Emirates">United Arab Emirates</option>
                                <option value="United Kingdom">United Kingdom</option>
                                <option value="United States">United States</option>
                                <option value="United States Minor Outlying Islands">United States Minor Outlying
                                    Islands
                                </option>
                                <option value="Uruguay">Uruguay</option>
                                <option value="Uzbekistan">Uzbekistan</option>
                                <option value="Vanuatu">Vanuatu</option>
                                <option value="Venezuela">Venezuela</option>
                                <option value="Viet Nam">Viet Nam</option>
                                <option value="Virgin Islands, British">Virgin Islands, British</option>
                                <option value="Virgin Islands, U.S.">Virgin Islands, U.S.</option>
                                <option value="Wallis and Futuna">Wallis and Futuna</option>
                                <option value="Western Sahara">Western Sahara</option>
                                <option value="Yemen">Yemen</option>
                                <option value="Zambia">Zambia</option>
                                <option value="Zimbabwe">Zimbabwe</option>
                            </select>
                        </div>
                    </fieldset>
                    <fieldset>
                        <div class="row">
                            <legend>Choix de la session de cours</legend>
                            <div class="col-md-6">
                                <label>Supports: </label>
                                <select class="form-select" aria-label="Default select example" name="support"
                                    id="support" v-model="support">
                                    <option selected value="tome1">Tome 1 de Médine</option>
                                    <option value="tome2">Tome 2 de Médine</option>
                                    <option value="tome3">Tome 3 de Médine</option>
                                    <option value="tome4">Tome 4 de Médine</option>
                                    <option value="alajouroumiyya">Alajouroumiyya</option>
                                    <option value="qatr">Qatr al nada</option>
                                    <option value="alfiyya">Alfiyya ibn maalik</option>
                                    <option value="vocabulaire">Vocabulaire débutants</option>
                                    <option value="coran">Coran</option>
                                    <option value="tajwid">Tajwid</option>
                                </select>
                            </div>
                            <div class="col-md-6">
                                <label>Type de session</label>
                                <select class="form-select" aria-label="Default select example" name="typeOfSession"
                                    id="typeOfSession" v-model="typeOfSession">
                                    <option selected value="individuelle">individuelle</option>
                                    <option value="collective">Collective</option>
                                </select>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-md-6">
                                <label class="mt-3">Fréquence des cours</label>
                                <select class="form-select" aria-label="Default select example" name="hoursPerWeek" id="hoursPerWeek" v-model="hoursPerWeek">
                                    <option selected value="1">1 heure</option>
                                    <option value="2">2 heures</option>
                                    <option value="3">3 heures</option>
                                    <option value="4">4 heures</option>
                                    <option value="5">5 heures</option>
                                    <option value="6">6 heures</option>
                                </select>
                            </div>
                            <div class="col-md-6">
                                <label class="mt-3">Choix du professeur</label>
                                <select class="form-select" aria-label="Default select example" name="prof" id="prof" v-model="prof">
                                    <option selected value="1">Arabophone / francophone</option>
                                    <option value="2">Uniquement arabophone</option>
                                </select>
                            </div>
                        </div>
                    </fieldset>
                    <div class="row">
                        <div class="col">
                            <legend class="mt-3">Comment avez-vous connu notre site ?</legend>
                            <select class="form-select" aria-label="Default select example" name="findOurWebsite" id="findOurWebsite" v-model="findOurWebsite">
                                <option selected value="1">Famille / Amis</option>
                                <option value="2">Facebook</option>
                                <option value="3">Twitter</option>
                                <option value="3">Instagram</option>
                                <option value="3">Moteur de recherche (Google, Bing, Yahoo)</option>
                                <option value="3">Via un autre site internet</option>
                                <option value="3">Autre</option>
                            </select>
                        </div>
                    </div>
                    <div class="mt-3 form-check">
                        <input class="form-check-input" type="checkbox" v-model="conditions" value="" id="flexCheckIndeterminate">
                        <label class="conditions form-check-label" for="flexCheckIndeterminate">
                            J'ai lu et accepte<span><a href="#"> les conditions générales</a></span>
                        </label>
                    </div>
                    <p id="erreur" style="color: red;"></p>
                    <button type="submit" class="mt-2 mb-3 btn btn-block bouton-form">Envoyer</button>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                equipments: [{
                        name: 'Un ordinateur performant, tablette ou smartphone'
                    },
                    {
                        name: 'Un casque avec microphone'
                    },
                    {
                        name: 'Un compte Zoom'
                    },
                ],
                errors: [],
                lastname: null,
                firstname: null,
                age: null,
                phone: null,
                email: null,
                verifemail: null,
                country: null,
                support: null,
                typeOfSession: null,
                hoursPerWeek: null,
                prof: null,
                findOurWebsite: null,
                conditions: null,
                output: ''
            }
        },
        methods: {
            checkForm: function (e) {
                e.preventDefault()

                let currentObject = this
                axios.post('https://localhost:8000/api/students', {
                    lastname: this.lastname,
                    firstname: this.firstname,
                    age: this.age,
                    phone: this.phone,
                    email: this.email,
                    verifemail: this.verifemail,
                    country: this.country,
                    support: this.support,
                    typeOfSession: this.typeOfSession,
                    hoursPerWeek: this.hoursPerWeek,
                    prof: this.prof,
                    findOurWebsite: this.findOurWebsite,
                    conditions: this.conditions
                })
                .then((response) => {
                    console.log(response.data)
                    currentObject.output = response.data
                })
                .catch((error) => {
                    currentObject.output = error
                })

                if (this.lastname && this.firstname && this.age && this.phone && this.email && this.verifemail && this.country && this.support && this.typeOfSession && this.hoursPerWeek && this.prof && this.findOurWebsite &&
                    this.conditions) {
                    return true
                }

                this.errors = []

                if (!this.lastname) {
                    this.errors.push('Le nom est requis')
                }
                if (!this.firstname) {
                    this.errors.push('Le prénom est requis')
                }
                if (!this.age) {
                    this.errors.push('L\'âge est requis')
                }
                if (!this.phone) {
                    this.errors.push('Le téléphone est requis')
                }
                if (!this.email) {
                    this.errors.push('L\'email est requis')
                }
                if (!this.verifemail) {
                    this.errors.push('La vérification de l\'email est requise')
                }
                if (!this.country) {
                    this.errors.push('Le pays est requis')
                }
                if (!this.support) {
                    this.errors.push('La support est requis')
                }
                if (!this.typeOfSession) {
                    this.errors.push('Le type de la session est requis')
                }
                if (!this.hoursPerWeek) {
                    this.errors.push('La fréquence de cours est requise')
                }
                if (!this.prof) {
                    this.errors.push('Le choix du professeur est requis')
                }
                if (!this.findOurWebsite) {
                    this.errors.push('Comment avez vous connu notre institut est requis')
                }
                if (!this.conditions) {
                    this.errors.push('Veuillez accepter les conditions générales')
                }
            },
        }
    }
</script>
<style scoped>
    button {
        background: #8CD9F1;
        color: #2c3e50;
    }
</style>