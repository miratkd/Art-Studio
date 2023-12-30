<template>
    <div class="component-container">
        <img class="component-img" :src="img" alt="">
        <div class="component-body">
            <h1 class="component-title">{{ title }}</h1>
            <div class="component-line"></div>
            <h3>{{ subTitle }}</h3>
            <p class="component-text">{{ text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PageFirst',
    props: ['img', 'title', 'subTitle', 'text']
}
</script>

<style scoped>
.component-container {
    height: 75vh;
    margin-top: 5vh;
    position: relative;
}

.component-img {
    height: 100%;
}

.component-body {
    position: absolute;
    bottom: 0;
    right: 0;
    width: 60%;
    height: 65%;
    background-color: white;
    box-sizing: border-box;
    padding-left: 12%;
}

.component-title {
    margin-top: -10%;
    margin-left: -30%;
}

.component-line {
    width: 10%;
    border-top: 0.3vh solid #C8CCD8;
    margin-bottom: 5vh;
    margin-top: 3vh;
}

.component-text {
    margin-top: 5vh;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .component-img {
        height: unset;
        width: 100%;
    }

    .component-container {
        height: unset;
    }

    .component-body {
        width: 90%;
        height: 55%;
    }

    .component-title {
        margin-top: -10%;
        margin-left: unset;
        text-align: end;
        font-size: 10em;
    }

    .component-line {
        margin-bottom: 3vh;
        margin-top: 1vh;
    }

    .component-text {
        margin-top: 2vh;
    }
}

/* mobile */
@media screen and (max-width: 500px) {
    
    .component-body{
        left: 0;
        right: unset;
        padding-top: 2vh;
        padding-left: 5%;
        margin-bottom: -30%;
    }
    .component-title{
        display: none;
    }
    .component-line{
        display: none;
    }
    .component-container{
        margin-bottom: 25vh;
    }
}
</style>