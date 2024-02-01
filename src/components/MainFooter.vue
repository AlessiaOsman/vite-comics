<script>
import MainNav from './MainNav.vue'
export default {
    name: 'MainFooter',
    components: {MainNav},
    methods: {
        // Funzione per creare la prima parte del path per l'immagine
        createImagePath(image) {
            const url = new URL(`../assets/img/${image}`, import.meta.url);
            return url.href

        }
    },
    data: ()=>({
        footerImage: 'dc-logo-bg.png'
    }),

}
</script>

<template>
    <div class="container">
        <div class="main-footer-row">
            <div class="main-footer-col">
                <h2>DC COMICS</h2>
                <MainNav/>
                <h2>SHOP</h2>
                <ul>
                    <li><a href="#">Shop DC</a></li>
                    <li><a href="#">Shop DC Collectibles</a></li>
                </ul>
            </div>
            <div class="main-footer-col">
                <h2>DC</h2>
                <MainNav/>
            </div>
            <div class="main-footer-col">
                <h2>SITES</h2>
                <MainNav/>
            </div>
        </div>
        <img :src="createImagePath(footerImage)" alt="logo">
    </div>
</template>

<style lang="scss">
.main-footer-row{
    display: flex;
    gap: 50px;
    margin-top: 45px;
}
.main-footer-col{
    ul{
        list-style-type: none;

        a{
            color: #ffffff;
        }
    }

    h2{
        color: #ffffff;
    }
}

</style>