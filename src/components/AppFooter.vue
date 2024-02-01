<script>
import MainFooter from './MainFooter.vue'
export default {
    name: 'AppFooter',
    components: {MainFooter},
    
    
}
</script>

<template>
    <footer>
        <div class="bonus">
            <div class="container"></div>
        </div>
        
            <MainFooter/>
        
        
        <div class="bonus2">
            <div class="container"></div>
        </div>
    </footer>
</template>

<style lang="scss">
    footer{
        flex-grow: 1;
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        position: relative;
    }

    .bonus{
        background-color: blue;
        min-height: 150px;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
    }

    .bonus2{
        background-color: green;
        min-height: 100px;
        position: absolute;
        bottom: 0;
        right: 0;
        left: 0;
    }
</style>