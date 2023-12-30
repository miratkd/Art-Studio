<template>
    <div>
        <p class="card-title">{{ info.name }}</p>
        <p>Mail : {{ info.email }}</p>
        <p>Address : {{ info.address }}</p>
        <p>Phone : {{ info.phone }}</p>
    </div>
</template>

<script>
export default {
    name: 'InfoCard',
    props: ['info']
}
</script>

<style scoped >
.card-title {
    font-weight: bold;
    margin-bottom: 2vh;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .card-title {
        margin-top: 4vh;
    }
}
</style>