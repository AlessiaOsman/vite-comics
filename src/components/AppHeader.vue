<script>
export default {
    name: 'AppHeader',
    // Aggiunto array di oggetti
    data: () => ({
        links: [
            {
                text: 'Characters',
                url: '#',
                current: false,
            },
            {
                text: 'Comics',
                url: '#',
                current: true,
            },
            {
                text: 'Movies',
                url: '#',
                current: false,
            },
            {
                text: 'TV',
                url: '#',
                current: false,
            },
            {
                text: 'Games',
                url: '#',
                current: false,
            },
            {
                text: 'Collectibles',
                url: '#',
                current: false,
            },
            {
                text: 'Videos',
                url: '#',
                current: false,
            },
            {
                text: 'Fans',
                url: '#',
                current: false,
            },
            {
                text: 'News',
                url: '#',
                current: false,
            },
            {
                text: 'Shop',
                url: '#',
                current: false,
            },
        ],
        logoImage: 'dc-logo.png'
    }),

    methods: {
        // Funzione per creare la prima parte del path per l'immagine
        createImagePath(image) {
            const url = new URL(`../assets/img/${image}`, import.meta.url);
            return url.href

        }
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