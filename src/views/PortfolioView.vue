<template>
    <div class="portfolio-container">
        <PortfolioBanner v-for="value in list" :key="value.title" :title="value.title" :text="value.year"
            :imgMob="value.mobImg" :img="value.img" />
    </div>
</template>

<script >
import PortfolioBanner from '@/components/PortfolioBanner.vue';
export default {
    name: 'PortfolioView',
    data() {
        return {
            list: [
                {
                    img: require('@/assets/port1.svg'),
                    mobImg: require('@/assets/port1mob.svg'),
                    title: 'Estação Seraph',
                    year: 'Setembro 2019'
                },
                {
                    img: require('@/assets/port2.svg'),
                    mobImg: require('@/assets/port2mob.svg'),
                    title: 'Edifício Eebox',
                    year: 'Agosto 2017'
                },
                {
                    img: require('@/assets/port3.svg'),
                    mobImg: require('@/assets/port3mob.svg'),
                    title: 'Torre Federal II',
                    year: 'Março 2019'
                },
                {
                    img: require('@/assets/port4.svg'),
                    mobImg: require('@/assets/port4mob.svg'),
                    title: 'Projeto Del Sol',
                    year: 'Janeiro 2016'
                },
                {
                    img: require('@/assets/port5.svg'),
                    mobImg: require('@/assets/port5mob.svg'),
                    title: 'Le Prototype',
                    year: 'Outubro 2015'
                },
                {
                    img: require('@/assets/port6.svg'),
                    mobImg: require('@/assets/port6mob.svg'),
                    title: 'Torre 228B',
                    year: 'Abril 2015'
                },
                {
                    img: require('@/assets/port7.svg'),
                    mobImg: require('@/assets/port7mob.svg'),
                    title: 'Hotel Grand Edelweiss',
                    year: 'Dezembro 2013'
                },
                {
                    img: require('@/assets/port8.svg'),
                    mobImg: require('@/assets/port8mob.svg'),
                    title: 'Torre Netcry',
                    year: 'Agosto 2012'
                },
                {
                    img: require('@/assets/port9.svg'),
                    mobImg: require('@/assets/port9mob.svg'),
                    title: 'Hypers',
                    year: 'Outubro 2015'
                },
                {
                    img: require('@/assets/port10.svg'),
                    mobImg: require('@/assets/port10mob.svg'),
                    title: 'Torre SXIV',
                    year: 'Março 2011'
                },
                {
                    img: require('@/assets/port11.svg'),
                    mobImg: require('@/assets/port11mob.svg'),
                    title: 'Torre Trinity Bank',
                    year: 'Setembro 2010'
                },
                {
                    img: require('@/assets/port12.svg'),
                    mobImg: require('@/assets/port12mob.svg'),
                    title: 'Projeto Paramour',
                    year: 'Fevereiro 2008'
                },

            ]
        }
    },
    components: {
        PortfolioBanner
    }
}
</script>

<style scoped>
.portfolio-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 3vh 2vw;
    margin-top: 2vh;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .portfolio-container {
        grid-template-columns: 1fr;
        gap: 3vh 0;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    .portfolio-container {
        margin: 0 5vw 2vh 5vw;
    }
}
</style>