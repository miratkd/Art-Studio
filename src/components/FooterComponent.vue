<template>
    <div class="footer-container">
        <div class="footer-select-container">
            <RouterLink to="/" class="footer-logo-container">
                <img class="footer-logo" src="@/assets/ArchLogo2.svg" alt="">
            </RouterLink>
            <RouterLink to="/portfolio">
                <p class="footer-link-text">Portfolio</p>
            </RouterLink>
            <RouterLink to="/about">
                <p class="footer-link-text">Sobre nos</p>
            </RouterLink>
            <RouterLink to="/contact" class="nav-desktop">
                <p class="footer-link-text">Contato</p>
            </RouterLink>
        </div>
        <ButtonFull :action="move" class="footer-button" text="Veja nosso portfólio" />
    </div>
</template>

<script>
import ButtonFull from './ButtonFull.vue';
export default {
    name: 'FooterComponent',
    components: {
        ButtonFull
    },
    methods: {
        move() {
            this.$router.push('portfolio')
        }
    }
}
</script>

<style scoped>
.footer-container {
    margin-top: 15vh;
    position: relative;
    display: flex;
    align-items: center;
}

.footer-select-container {
    background: #EEEFF4;
    width: 90%;
    height: 13vh;
    display: flex;
    align-items: center;
    gap: 10%;
}

.footer-link-text {
    color: #7D828F;
    font-weight: 700;
}

.footer-logo-container {
    background-color: #1B1D23;
    height: 100%;
    width: 15%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.footer-logo {
    width: 60%;
}

.footer-button {
    position: absolute;
    right: 0;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .footer-container {
        margin-left: -12vw;
        width: 121%;
    }

    .footer-select-container {
        gap: 8%;
        width: 75%;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    .footer-container {
        margin-left: 0;
        width: 100%;
        flex-direction: column;
    }
    .footer-select-container {
        gap: 2.5vh;
        width: 100%;
        flex-direction: column;
        height: 32vh;
    }

    .footer-button {
        bottom: 0;
        right: unset;
    }
    .footer-logo-container{
        height: 10vh;
        width: 10vh;
        margin-top: -4vh;
    }
}</style>