<template>
    <nav class="nav-container">
        <RouterLink to="/">
            <img src="@/assets/ArchLogo.svg" alt="Logo">
        </RouterLink>
        <RouterLink to="/portfolio">
            <p :class="{ 'active-page': page == 'portfolio' }">Portfolio</p>
            <div :class="{ 'active-line': page == 'portfolio' }" class="under-line"></div>
        </RouterLink>
        <RouterLink to="/about">
            <p :class="{ 'active-page': page == 'about' }">Sobre nos</p>
            <div :class="{ 'active-line': page == 'about' }" class="under-line"></div>
        </RouterLink>
        <RouterLink to="/contact">
            <p :class="{ 'active-page': page == 'contact' }">Contato</p>
            <div :class="{ 'active-line': page == 'contact' }" class="under-line"></div>
        </RouterLink>
    </nav>
</template>

<script>
export default {
    name: 'AppNav',
    data() {
        return {
            page: this.$route.name
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
    margin-bottom: 3vh;
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
}</style>