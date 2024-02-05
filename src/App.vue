<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import { headerLinks, products, footerMenus, upperFooterLinks, iconLinks } from './assets/data/index';

export default {
  name: 'Comics',
  components: { AppHeader, AppMain, AppFooter },
  data: () => ({
    headerLinks,
    products,
    footerMenus,
    upperFooterLinks,
    iconLinks
  })


}
</script>

<template>
  <AppHeader :links="headerLinks" />
  <AppMain />
  <AppFooter :menus="footerMenus" :upper-menus="upperFooterLinks" />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
