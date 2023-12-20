<template>
    <div class="welcome-container">
        <img class="welcome-img" src="@/assets/welcome.svg" alt="">
        <div class="welcome-title-container">
            <h1 class="welcome-title">Bem vindo</h1>
            <div class="welcome-text-container">
                <h3>Bem vindo ao estúdio Arch</h3>
                <br><br><br>
                <p>Temos uma rede única e um conjunto de habilidades para ajudar a dar vida aos seus projetos. Nossa pequena
                    equipe de indivíduos altamente qualificados combinada com nossa grande rede nos coloca em uma posição
                    forte para entregar resultados excepcionais. <br> <br>

                    Nos últimos 10 anos, trabalhamos em todos os tipos de projetos. De estações a arranha-céus, criamos
                    espaços que inspiram e encantam. <br><br>

                    Trabalhamos em estreita colaboração com nossos clientes para que entendamos os meandros de cada projeto.
                    Isso nos permite trabalhar em harmonia para criar projetos verdadeiramente
                    impressionantes que resistirão ao teste do tempo.</p>

            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeWelcome'
}
</script>

<style scoped>
.welcome-container {
    margin-top: 15vh;
    position: relative;
    height: 80vh;
}

.welcome-title-container {
    position: absolute;
    top: -4vh;
    z-index: 2;
}

.welcome-img {
    height: 100%;
    position: absolute;
    right: 0;
    z-index: 1;
}

.welcome-title {
    line-height: 0.5;
}

.welcome-text-container {
    margin-left: 8%;
    width: 45%;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .welcome-img {
        display: none;
    }

    .welcome-text-container {
        margin-left: 0;
        width: 100%;
    }
    .welcome-title{
        font-size: 8.5em;
        line-height: unset;
    }
}

/* mobile */
@media screen and (max-width: 500px ){
    .welcome-text-container {
        margin-left: 5vw;
        width: 90%;
    }
    .welcome-title{
        display: none;
    }
}</style>