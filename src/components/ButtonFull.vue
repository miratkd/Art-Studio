<template>
    <button class="button-container" v-on:click="action">
        {{ text }}
        <span class="material-icons" style="font-size: 2em;">arrow_forward</span>
    </button>
</template>

<script>
export default {
    name: 'ButtonFull',
    props:['text', 'action']
}
</script>

<style scoped>
.button-container{
    display: flex;
    background: #1B1D23;
    color: white;
    align-items: center;
    justify-content: center;
    gap: 10%;
    outline: none;
    border: none;
    padding: 1.5vh 2vw;
    cursor: pointer;
    text-wrap: nowrap;
    font-size: 1.2em;
}
.button-container:hover{
    background: #60636D;
}

/* tablet */
@media screen and (max-width: 1050px ) and (orientation: portrait){
    .button-container{
        padding: 1.5vh 5vw;
    }
}
</style>