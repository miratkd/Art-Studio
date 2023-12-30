<template>
    <p :class="{'alert-show': alertShow}" class="alert-container">
        Mensagem enviada!
    </p>
</template>

<script>
export default {
    name: 'MessageAlert',
    props: ['alertShow']
}
</script>

<style scoped>
.alert-container{
    position: fixed;
    top: 10vh;
    left: 100vw;
    background: #1B1D23;
    color: white;
    padding: 1.5vh 3vw;
    transition: left 1s;
    width: max-content;
}
.alert-show{
    left: 70vw;
}

/* mobile */
@media screen and (max-width: 500px) {
    .alert-show{
    left: 60vw;
}
}
</style>