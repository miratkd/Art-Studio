<template>
    <div class="form-container">
        <h3>Entre em <br> contato</h3>
        <div class="form-rigth">
            <input v-model="name" placeholder="Nome" :class="{ 'form-error-input': nameError }" class="form-input "
                type="text">
            <p class="form-error-message">{{ nameError }}</p>
            <input v-model="email" placeholder="Email" :class="{ 'form-error-input': emailError }" class="form-input"
                type="text">
            <p class="form-error-message">{{ emailError }}</p>
            <textarea v-model="text" :class="{ 'form-error-input': textError }" style="margin-bottom: 0;" class="form-input"
                placeholder="Mensagem" name="" id="" rows="6"></textarea>
            <button v-on:click="send()" class="form-button" type="button">
                <span class="material-icons">arrow_forward</span>
            </button>
            <p class="form-error-message">{{ textError }}</p>
        </div>


        <MessageAlert :alertShow="alertShow"/>
    </div>
</template>

<script>
import MessageAlert from './MessageAlert.vue'
export default {
    name: 'ContactForm',
    data() {
        return {
            name: '',
            email: '',
            text: '',
            nameError: '',
            emailError: '',
            textError: '',
            alertShow: false
        }
    },
    components:{
        MessageAlert
    },
    watch: {
        name() { this.nameError = '' },
        email() { this.emailError = '' },
        text() { this.textError = '' }
    },
    methods: {
        send() {
            if (!this.name) this.nameError = 'Por favor, insira seu nome.'
            if (!this.email) this.emailError = 'Por favor, insira seu email.'
            if (!this.text) this.textError = 'Por favor insira uma mensagem.'
            if (!this.validateEmail(this.email)) this.emailError = 'Por favor, insira um email valido.'
            if (this.validateEmail(this.email) && this.name && this.text) {
                this.alertShow = true
                setTimeout(() => this.alertShow = false, 5000);
            }
        },
        validateEmail(email) {
            var re = /\S+@\S+\.\S+/;
            return re.test(email);
        }
    }
}
</script>
<style scoped>
.form-container {
    margin-top: 15vh;
    display: flex;
    justify-content: space-between;
}

.form-rigth {
    width: 55%;
    display: flex;
    flex-direction: column;
}

.form-input {
    margin-bottom: 2vh;
    color: #1B1D23;
    width: 100%;
    font-size: 1.2em;
    font-weight: 700;
    border: none;
    border-bottom: #C8CCD8 2px solid;
    padding-left: 2vw;
    padding-bottom: 2vh;
    box-sizing: border-box;
}

.form-input:focus {
    outline: none;
    border-bottom: #1B1D23 2px solid;
}

::placeholder {
    color: #C8CCD8;
    opacity: 1;
    /* Firefox */
}

::-ms-input-placeholder {
    /* Edge 12 -18 */
    color: #C8CCD8;
}

.form-button {
    width: 5vw;
    height: 5vw;
    background-color: #1B1D23;
    border: none;
    color: white;
    cursor: pointer;
    margin-left: auto;
}

.form-button:hover {
    background-color: #60636D;
}

.form-error-message {
    color: #DF5656;
    font-weight: bold;
}

.form-error-input {
    border-bottom: #DF5656 2px solid;
}

.form-error-input::placeholder {
    color: #DF5656;
}

.form-error-input::-ms-input-placeholder {
    color: #DF5656;
}
/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .form-container{
        flex-direction: column;
        gap: 5vh;
    }
    .form-rigth{
        width: 100%;
    }
}
/* mobile */
@media screen and (max-width: 500px) {
    .form-container{
        padding: 0 5vw;
    }
    .form-button{
        width: 10vw;
        height: 10vw;
    }
}
</style>