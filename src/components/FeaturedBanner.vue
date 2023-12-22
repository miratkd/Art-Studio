<template>
    <div class="banner-container">
        <img class="banner-img" :src="img" alt="">
        <img class="banner-mobile-img" :src="imgMobile" alt="">
        <div class="banner-text-container">
            <h4 style="color: white;">{{ text }}</h4>
            <p v-on:click="move()" class="banner-link" style="color: white;">Ver todos os projetos</p>
        </div>
        <h1 class="banner-mobile-number">{{ number }}</h1>
    </div>
</template>

<script>
export default {
    name: 'FeaturedBanner',
    props: ['img', 'text', 'imgMobile', 'number'],
    methods: {
        move() {
            this.$router.push('portfolio')
        }
    }
}
</script>

<style scoped>
.banner-container {
    height: 55vh;
    max-height: 37vw;
    position: relative;
}

.banner-img {
    height: 100%;
}

.banner-text-container {
    left: 10%;
    bottom: 10%;
    position: absolute;
}

.banner-link:hover {
    cursor: pointer;
    text-decoration: underline;
}

.banner-mobile-img {
    display: none;
}

.banner-mobile-number {
    display: none;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .banner-img {
        display: none;
    }

    .banner-mobile-img {
        display: flex;
        width: 100%;
    }

    .banner-container {
        height: unset;
        max-width: unset;
    }

    .banner-mobile-number {
        display: block;
        opacity: 0.5;
        right: 5%;
        position: absolute;
        z-index: 3;
        top: 15%;
    }
}
/* mobile */
@media screen and (max-width: 500px ){
    .banner-container {
        height: 35vh;
        max-height: unset;
        overflow: hidden;
    }
    .banner-mobile-img {
        width: unset;
        height: 100%;
    }
    .banner-mobile-number{
        display: none;
    }
}
</style>