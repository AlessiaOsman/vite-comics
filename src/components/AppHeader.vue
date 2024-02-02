<script>
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
    props: {
        links: Array

    }
}
</script>

<template>
    <header>
        <div class="container">

            <img :src="createImagePath(logoImage)" alt="logo">
            <ul>
                <li v-for="link in links"><a :href="link.url">{{ link.text }}</a></li>
            </ul>

        </div>

    </header>
</template>

<style lang="scss" scoped>
header {
    background-color: #ffffff;
    padding: 24px 0;


    ul {
        display: flex;
        gap: 16px;
        list-style-type: none;
        font-weight: bold;
        text-transform: uppercase;

        a {
            color: #000000;
        }
    }
}
</style>