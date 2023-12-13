<template>
    <div class="tag-container">
        <div class="tag-line"></div>
        <p class="tag-text">{{ pageName }}</p>
    </div>
</template>

<script>
export default {
    name: 'SideTagComponent',
    computed:{
        pageName(){
            if(this.$route.name == 'home') return 'home'
            else if (this.$route.name == 'portfolio') return 'portfolio'
            else if (this.$route.name == 'about') return 'sobre'
            return 'contato'
        }
    }
}
</script>

<style scoped>
.tag-container{
    position: absolute;
    top: 0;
    left: 4vw;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.tag-line{
    border: 1px solid #C8CCD8;
    height: 10vh;
}
.tag-text{
    text-transform: uppercase;
    writing-mode: vertical-rl;
    text-orientation: mixed;
    color: #C8CCD8;
    font-weight: 500;
    letter-spacing: 18px;
    margin-top: 2vh;
}

/* mobile */
@media screen and (max-width: 500px ){
    .tag-container{
        display: none;
    }
}
</style>