<script>
import MainNav from './MainNav.vue'
export default {
    name: 'AppHeader',
    // Aggiunto array di oggetti
    data: () => ({
        
        logoImage: 'dc-logo.png'
    }),

    methods: {
        // Funzione per creare la prima parte del path per l'immagine
        createImagePath(image) {
            const url = new URL(`../assets/img/${image}`, import.meta.url);
            return url.href

        }
    },
    components: {MainNav}
}
</script>

<template>
    <header>
        <div class="container">

            <img :src="createImagePath(logoImage)" alt="logo">
            <MainNav/>
            
        </div>

    </header>
</template>

<style lang="scss">
header {
    background-color: #ffffff;
    padding: 24px 0;
    

    ul {
        display: flex;
        gap: 16px;
        list-style-type: none;
        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>