<template>
    <div class="contact-img-container">
        <img class="contact-img" src="@/assets/map.svg" alt="">
    </div>
</template>

<script>
export default {
    name: 'ContactImg'
}
</script>

<style scoped>
.contact-img-container{
    margin-top: 15vh;
    width: 100%;
}
.contact-img{
    width: 100%;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .contact-img-container{
    display: flex;
    justify-content: center;
    overflow: hidden;
    margin-top: 10vh;
}
.contact-img{
    width: 175%;
    margin-right: 20%;
}
}
</style>