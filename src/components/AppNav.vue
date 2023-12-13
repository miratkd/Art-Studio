<template>
    <div v-on:click="isMenuOpen = false">
        <nav class="nav-container">
            <RouterLink to="/">
                <img class="nav-img" src="@/assets/ArchLogo.svg" alt="Logo">
            </RouterLink>
            <RouterLink to="/portfolio" class="nav-desktop">
                <p :class="{ 'active-page': page == 'portfolio' }">Portfolio</p>
                <div :class="{ 'active-line': page == 'portfolio' }" class="under-line"></div>
            </RouterLink>
            <RouterLink to="/about" class="nav-desktop">
                <p :class="{ 'active-page': page == 'about' }">Sobre nos</p>
                <div :class="{ 'active-line': page == 'about' }" class="under-line"></div>
            </RouterLink>
            <RouterLink to="/contact" class="nav-desktop">
                <p :class="{ 'active-page': page == 'contact' }">Contato</p>
                <div :class="{ 'active-line': page == 'contact' }" class="under-line"></div>
            </RouterLink>
            <span class="material-icons nav-mobile-icon" v-on:click.stop="isMenuOpen = !isMenuOpen">menu</span>
        </nav>
        <div  v-if="isMenuOpen" class="mobile-menu">
            <RouterLink to="/portfolio" >
                <h4>Portfolio</h4>
            </RouterLink>
            <RouterLink to="/about" >
                <h4>Sobre nos</h4>
            </RouterLink>
            <RouterLink to="/contact" >
               <h4>Contato</h4> 
            </RouterLink>
            
        </div>
        <div v-if="isMenuOpen" class="mobile-menu-background"></div>
    </div>
</template>

<script>
export default {
    name: 'AppNav',
    data() {
        return {
            page: this.$route.name,
            isMenuOpen: false
        }
    },
    watch: {
        $route(value) {
            this.page = value.name
        }
    }
}
</script>
<style scoped>
.nav-container {
    display: flex;
    align-items: center;
    gap: 5vw;
    height: 5vh;
    background-color: white;
    position: relative;
}

p {
    font-weight: bold;
    padding-bottom: calc(1vh + 2px);
}

a {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.active-page {
    color: #1B1D23;
}

.under-line {
    border-bottom: 3px solid transparent;
    width: 50%;
}

.active-line {
    border-color: #1B1D23;
}

.nav-img {
    width: 4em;
    margin-top: -2vh;
}

.nav-mobile-icon {
    display: none;
}

/* tablet */
@media screen and (max-width: 1050px) and (orientation: portrait) {
    .nav-container {
        gap: 15%;
    }

}

/* mobile */
@media screen and (max-width: 500px) {
    .nav-desktop {
        display: none;
    }

    .nav-mobile-icon {
        display: block;
        font-size: 3em;
        cursor: pointer;
    }

    .nav-img {
        margin-top: 0;
    }

    .nav-container {
        position: fixed;
        height: 10vh;
        z-index: 5;
        width: 100%;
        top: 0;
        justify-content: space-between;
        padding: 0 5%;
        box-sizing: border-box;
    }

    .mobile-menu-background {
        position: fixed;
        z-index: 2;
        top: 0;
        height: 100dvh;
        width: 100%;
        opacity: 0.5;
        background: #000;
    }
    .mobile-menu{
        background-color: white;
        position: fixed;
        z-index: 3;
        width: 80%;
        height: 20vh;
        top: 10vh;
        right: 0;
        box-sizing: border-box;
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
    }
}</style>