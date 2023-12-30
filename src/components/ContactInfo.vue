<template>
    <div>
        <div class="contact-line"></div>
        <div class="contact-container">
            <h2 class="contact-left">Informações de contato</h2>
            <InfoCard
                :info="{ name: 'Escritório principal', email: 'archone@mail.com', address: '1892 Chenoweth Drive TN', phone: '123-456-3451' }" />
            <InfoCard
                :info="{ name: 'Escritório II', email: 'archtwo@mail.com', address: '3399 Wines Lane TX', phone: '832-123-4321' }" />
        </div>
    </div>
</template>

<script>
import InfoCard from './InfoCard.vue';
export default {
    name: 'ContactInfo',
    components: {
        InfoCard
    }
}
</script>

<style scoped>
.contact-container {
    display: flex;
    justify-content: space-between;
}

.contact-left {
    width: 45%;
}

.contact-line {
    width: 20%;
    border-top: 0.3vh solid #C8CCD8;
    margin-top: 12vh;
    margin-bottom: 8vh;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .contact-left {
        width: 80%;
    }

    .contact-container {
        flex-direction: column;
    }

}

/* mobile */
@media screen and (max-width: 500px) {
    .contact-container {
        padding: 0 5vw;
    }

    .contact-left {
        font-size: 5em;
    }

    .contact-line {
        display: none;
    }
}</style>