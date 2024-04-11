<script>
import AppHeader from './components/AppHeader.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMainContent,
    AppFooter
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppMainContent></AppMainContent>
  </main>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './style/generic';
</style>