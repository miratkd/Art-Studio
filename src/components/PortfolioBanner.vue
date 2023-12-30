<template>
    <div class="banner-container">
        <img class="banner-img" :src="img" alt="">
        <img class="banner-mobile-img" :src="imgMob" alt="">
        <div class="banner-text-container">
            <h4 style="color: white;">{{ title }}</h4>
            <p style="color: white; opacity: 0.75;">{{ text }}</p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'PortfolioBanner',
    props: ['img', 'title', 'text', 'imgMob']
}
</script>

<style scoped>
.banner-container {
    position: relative;
}

.banner-img {
    width: 100%;
}

.banner-text-container {
    position: absolute;
    top: 80%;
    left: 15%;
}

.banner-mobile-img {
    display: none;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .banner-img {
        display: none;
    }

    .banner-mobile-img {
        display: block;
        width: 100%;
    }

    .banner-text-container {
        position: absolute;
        top: 60%;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    .banner-mobile-img {
        height: 100%;
        width: unset;
        margin-left: -20%;
    }

    .banner-container {
        height: 30vh;
        overflow: hidden;
    }
}
</style>