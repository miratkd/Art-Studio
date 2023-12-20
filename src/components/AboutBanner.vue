<template>
    <div class="about-container">
        <img class="about-img" src="@/assets/about.svg" alt="">
        <div class="about-darken"></div>
        <div class="about-contant">
            <h3 style="color: white; margin-bottom: 3vh;">Pequenas equipes, <br> grandes ideias</h3>
            <ButtonFull :action="move" text="Sobre nós" />
        </div>
    </div>
</template>

<script>
import ButtonFull from './ButtonFull.vue';
export default {
    name: 'AboutBanner',
    components: {
        ButtonFull
    },
    methods: {
        move() {
            this.$router.push('about')
        }
    }
}
</script>

<style scoped>
.about-container {
    margin-top: 5vh;
    position: relative;
}

.about-img {
    width: 100%;
}

.about-darken {
    position: absolute;
    top: 0;
    width: 100%;
    height: 99.5%;
    background-color: black;
    opacity: 0.5;
    z-index: 1;
}

.about-contant {
    position: absolute;
    z-index: 2;
    top: 27%;
    left: 15%;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .about-container {
        height: 45vh;
        overflow: hidden;
    }

    .about-img {
        width: auto;
        height: 100%;
    }
}
/* mobile */
@media screen and (max-width: 500px ){
    .about-contant {
    left: 10%;
    top: 20%;
}
}</style>