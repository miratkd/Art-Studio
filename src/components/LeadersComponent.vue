<template>
    <div class="leaders-container">
        <h2 class="leaders-left">Nossos lideres</h2>
        <div class="leaders-right">
            <LeaderCard :leader="leader" v-for="leader in list" :key="leader.name" />
        </div>
    </div>
</template>

<script>
import LeaderCard from './LeaderCard.vue';
export default {
    name: 'LeadersComponent',
    components: {
        LeaderCard
    },
    data() {
        return {
            list: [
                {
                    name: 'Jake Richards',
                    job: 'Arquiteto chefe',
                    img: require('@/assets/jakeImg.svg')
                },
                {
                    name: 'Thompson Smith',
                    job: 'Financeiro',
                    img: require('@/assets/thompsonImg.svg')
                },
                {
                    name: 'Jackson Rourke',
                    job: 'Designer chefe',
                    img: require('@/assets/jacksonImg.svg')
                },
                {
                    name: 'Maria Simpson',
                    job: 'Arquiteta sênior',
                    img: require('@/assets/mariaImg.svg')
                }
            ]
        }
    }
}
</script>

<style scoped>
.leaders-container {
    margin-top: 15vh;
    display: flex;
    justify-content: space-between;
}

.leaders-right {
    width: 65%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 5vh 2vw;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .leaders-container {
        flex-direction: column;
    }

    .leaders-left {
        margin-bottom: 5vh;
    }

    .leaders-right {
        width: 100%;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    .leaders-right {
        grid-template-columns: 1fr;
        gap: 5vh 0;
    }
    .leaders-container {
        padding: 0 5vw;
    }
}
</style>