<script>
import AppHeader from './components/AppHeader.vue';
import ComicsList from './components/ComicsList.vue';
import AppMainBuy from './components/AppMainBuy.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    ComicsList,
    AppMainBuy,
    AppFooter
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <ComicsList></ComicsList>
    <AppMainBuy></AppMainBuy>
  </main>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './style/generic';
</style>