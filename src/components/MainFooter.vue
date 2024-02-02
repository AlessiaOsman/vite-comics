<script>
export default {
    name: 'MainFooter',
    methods: {
        // Funzione per creare la prima parte del path per l'immagine
        createImagePath(image) {
            const url = new URL(`../assets/img/${image}`, import.meta.url);
            return url.href

        }
    },
    data: () => ({
        footerImage: 'dc-logo-bg.png'
    }),

}
</script>

<template>
    <div class="container">
        <div class="main-footer-row">
            <div class="main-footer-col">
                <h2>DC COMICS</h2>
                
            </div>
            <div class="main-footer-col">
                <h2>DC</h2>
                
            </div>
            <div class="main-footer-col">
                <h2>SITES</h2>
              
            </div>
        </div>
        <img :src="createImagePath(footerImage)" alt="logo">
    </div>
</template>

<style lang="scss" scoped>
.container {
    padding: 70px 0;

.main-footer-row {
    display: flex;
    gap: 50px;
    margin-top: 45px;

    h2 {
        color: #ffffff;
        margin: 16px 0;
    }

    ul {
        list-style-type: none;
        display: flex;
        flex-direction: column;
        gap: 8px;

            a {
                color: #ffffff;
            }
        
    }
}
}
</style>