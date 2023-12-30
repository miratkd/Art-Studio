<template>
    <div class="heritage-container">
        <div class="heritage-left">
            <div class="heritage-line"></div>
            <h2>Nosso legado</h2>
            <p>Fundada em 2007, nos começamos como um trio de arquitetos. nossas habilidades complementares e atenção a
                detalhes tornaram a Arch uma das empresas mais procuradas do pais. <br> <br> Se especializar em design
                urbano nos permitiu focar em criar estruturas excepcionais que vivem em harmonia com o ambiente. Nos
                consideramos cada detalhe do ambiente para o nosso projeto. <br> <br> Nosso pequeno time de profissionais
                internacionais contribui para cada projeto.</p>
        </div>
        <img class="heritage-img" src="@/assets/heritageImg.svg" alt="">
    </div>
</template>

<script>
export default {
    name: 'AboutHeritage'
}
</script>

<style scoped>
.heritage-container {
    margin-top: 15vh;
    display: flex;
    justify-content: space-between;
}

.heritage-line {
    width: 20%;
    border-top: 0.3vh solid #C8CCD8;
}

.heritage-left {
    width: 45%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.heritage-img {
    width: 45%;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .heritage-img {
        display: none;
    }

    .heritage-left {
        width: 100%;
        gap: 5vh;
    }


}

/* mobile */
@media screen and (max-width: 500px) {
    .heritage-container {
        padding: 0 5vw;
    }
}</style>