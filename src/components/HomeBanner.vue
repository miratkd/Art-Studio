<template>
    <div class="banner-container">
        <img v-show="page==1" class="banner-img" src="@/assets/Bitmap.svg" alt="">
        <img v-show="page==2" class="banner-img" src="@/assets/Bitmap2.svg" alt="">
        <img v-show="page==3" class="banner-img" src="@/assets/Bitmap3.svg" alt="">
        <img v-show="page==4" class="banner-img" src="@/assets/Bitmap4.svg" alt="">
        <div class="darken-layer"></div>
        <div class="banner-text-container">
            <h2 class="banner-title">{{ bannerList[page-1].title }}</h2>
            <p class="banner-text">{{ bannerList[page-1].text }}</p>
            <ButtonFull :action="move" :text=" bannerList[page-1].button "/>
        </div>
        <div class="banner-select-container">
            <button :class="{'banner-selected-button': page==1}" class="banner-select-button " v-on:click="page = 1">1</button>
            <button :class="{'banner-selected-button': page==2}" class="banner-select-button" v-on:click="page = 2">2</button>
            <button :class="{'banner-selected-button': page==3}" class="banner-select-button" v-on:click="page = 3">3</button>
            <button :class="{'banner-selected-button': page==4}" class="banner-select-button" v-on:click="page = 4">4</button>
        </div>
    </div>
</template>

<script>
import ButtonFull from './ButtonFull.vue';

export default {
    name: 'HomeBanner',
    data(){
        return {
            page: 1,
            bannerList:[
                {
                   title: 'Projeto Paramour',
                   text: 'Projeto feito para um museu de arte no sudoeste de Londres, Projeto Paramour é um simbolo de arquitetura moderna.',
                   button: 'Veja o nosso portfolio'
                },
                {
                   title: 'Estação Seraph',
                   text: 'O projeto Seraph nos desafiou a projetar uma estação unica que transporte as pessoas através do tempo. O resultado é um modelo novo e futurista inspirado pela estação espacial',
                   button: 'Veja o nosso portfolio'
                },
                {
                   title: 'Torre Federal II',
                   text: 'Uma sequencia para o projeto da torre originalmente construído em 1800. Nos alcançamos isso com um forte olhar de minimalismo brutal e toques modernos',
                   button: 'Veja o nosso portfolio'
                },
                {
                   title: 'Torre Trinity Bank',
                   text: 'A Trinity Bank nos desafiou a criar um conceito para um edifício dos anos 84 localizado no centro de uma cidade com altas taxas de terremoto. para esse projeto nos usamos curvas para camuflar design e estabilidade.',
                   button: 'Veja o nosso portfolio'
                },
            ]
        }
    },
    components:{
        ButtonFull
    },
    methods:{
        move(){
            this.$router.push('portfolio')
        }
    }
}
</script>

<style scoped>
.banner-container{
    margin-top: 2vh;
    position: relative;
    width: 100%;
}
.banner-img{
    width: 100%;
    height: 100%;
}
.darken-layer{
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 1;
    background-color: black;
    opacity: 0.5;
    top: 0;
}
.banner-select-container{
    position: absolute;
    z-index: 1;
    bottom: 0;
    left: -4vw;
    display: flex;
}
.banner-select-button{
    width: 4vw;
    height: 4vw;
    border: none;
    outline: none;
    background-color: white;
    color: #7D828F;
    font-weight: bold;
    font-size: 1.1em;
    cursor: pointer;
}
.banner-select-button:hover{
    background-color: #EEEFF4;
}
.banner-selected-button{
    background-color: #1B1D23 !important;
    color: white ;
}
.banner-text-container{
    position: absolute;
    z-index: 2;
    top: 20%;
    left: 20%;
}
.banner-text{
    color: white;
    height: 15vh;
    width: 45%;
}
.banner-title{
    color: white;
    width: 52%;
    margin-bottom: 1.5vh;
}

/* tablet */
@media screen and (max-width: 1050px ) and (orientation: portrait) {
    .banner-container{
        height: 60vh;
        overflow: hidden;
    }
    .banner-img{
        width: auto;
        height: 100%;
    }
    .banner-select-container{
        left: 0;
    }
    .banner-select-button{
        width: 7vw;
        height: 7vw;
    }
    .banner-text{
        width: 70%;
    }
    .banner-text-container{
        top: 10%;
        left: 10%;
    }
    .banner-title{
        width: 95%;
    }
}
/* mobile */
@media screen and (max-width: 500px ){
    .banner-text-container{
        left: 5%;
    }
}
</style>