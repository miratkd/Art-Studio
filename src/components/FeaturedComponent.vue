<template>
    <div class="featured-container">
        <div class="featured-title-row">
            <h2 class="featured-mobile-title">Destaques</h2>
            <ButtonFull class="featured-desktop-button" :action="move" text="Ver todos" />
        </div>
        <div class="featured-body-row">
            <FeaturedBanner text="Projeto Del Sol" number="1" :img="require('@/assets/featured1.svg')"
                :imgMobile="require('@/assets/featured1mobile.svg')" />
            <FeaturedBanner text="Torre 228B" number="2" :img="require('@/assets/featured2.svg')"
                :imgMobile="require('@/assets/featured2mobile.svg')" />
            <FeaturedBanner text="Le Prototype" number="3" :img="require('@/assets/featured3.svg')"
                :imgMobile="require('@/assets/featured3mobile.svg')" />
        </div>
        <ButtonFull class="featured-mobile-button" :action="move" text="Ver todos" />
    </div>
</template>

<script>
import ButtonFull from './ButtonFull.vue';
import FeaturedBanner from './FeaturedBanner.vue';

export default {
    name: 'FeaturedComponent',
    components: {
        ButtonFull,
        FeaturedBanner
    },
    methods: {
        move() {
            this.$router.push('portfolio')
        }
    }
}
</script>

<style scoped>
.featured-container {
    margin-top: 15vh;
}

.featured-title-row {
    display: flex;
    justify-content: space-between;
    margin-bottom: 4vh;
}

.featured-body-row {
    display: flex;
    justify-content: space-between;
}

.featured-mobile-button {
    display: none;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .featured-mobile-title {
        font-size: 4.5em;
    }

    .featured-body-row {
        display: flex;
        flex-direction: column;
        gap: 3vh;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    .featured-desktop-button {
        display: none;
    }

    .featured-mobile-button {
        display: flex;
        margin-top: 4vh;
        width: 100%;
    }
}
</style>