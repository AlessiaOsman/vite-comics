<script>
import FooterMenu from './FooterMenu.vue'
export default {
    name: 'AppFooter',
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
    props: {
        menus: Array,
        upperMenus: Array

    },

    components: { FooterMenu }


}
</script>

<template>
    <footer>
        <div class="upper-footer">
            <div class="container">
                <ul class="upper-footer-menu">
                    <li v-for="menu in upperMenus" :key="menu.id">
                        <img :src="createImagePath(menu.img)" :alt="menu.text">
                        <a href="#">{{ menu.text }}</a>
                    </li>
                </ul>
            </div>
        </div>

        <div class="container">
            <div class="main-footer-row">
                <div v-for="(menu, i) in menus" :key="i" class="main-footer-col">
                   <FooterMenu :title="menu.title" :links="menu.links"/>
                </div>
            </div>
            <img :src="createImagePath(footerImage)" alt="logo">
        </div>


        <div class="bottom-footer">
            <div class="container">
                <button>SIGN UP NOW</button>
                
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    flex-grow: 1;
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}

.upper-footer {
    background-color: #0282f9;
    min-height: 150px;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    display: flex;

    ul{
        display: flex;
        list-style-type: none;
        width: 100%;

        li{
            display: flex;
            align-items: center;
            flex-basis: 25%;
            justify-content: center;
            gap: 8px;

            img{
                width:50px;
                height: auto;
            }

            a{
                color: #ffffff;
            }
        }
    }
}

.bottom-footer {
    background-color: #303030;
    min-height: 100px;
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
}

.main-footer-row {
    display: flex;
    gap: 50px;
    margin-top: 45px;


}
</style>