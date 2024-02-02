<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import { menusLinks, products } from './assets/data/index';

export default {
  name: 'Comics',
  components: { AppHeader, AppMain, AppFooter },
  data: ()=>({
    menusLinks,
    products
  })


}
</script>

<template>
  <AppHeader :links="menusLinks" />
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
