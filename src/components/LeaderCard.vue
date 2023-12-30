<template>
    <div class="card-container">
        <div class="card-img-container">
            <img class="card-img" :src="leader.img" alt="">
            <img class="card-logo" src="@/assets/leaderLogo.svg" alt="">
        </div>
        <h4 style="margin-top: 2vh;">{{ leader.name }}</h4>
        <p>{{ leader.job }}</p>
    </div>
</template>

<script>
export default {
    name: 'LeaderCard',
    props: ['leader']
}
</script>

<style scoped>
.card-img {
    width: 100%;
    cursor: pointer;
}

.card-logo {
    position: absolute;
    top: 10vw;
    left: 8vw;
    z-index: 1;
    cursor: pointer;
    display: none;
}

.card-img-container {
    position: relative;
}


/* desktop */
@media screen and (orientation: landscape) {
    .card-img-container:hover>.card-img {
        filter: brightness(30%);
    }

    .card-img-container:hover>.card-logo {
        display: block;
    }
}</style>