<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppMainBuy from './components/AppMainBuy.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMainContent,
    AppMainBuy,
    AppFooter
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppMainContent></AppMainContent>
    <AppMainBuy></AppMainBuy>
  </main>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './style/generic';
</style>