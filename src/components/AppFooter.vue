<script>
import AppFooterLink from './AppFooterLink.vue';
import AppFooterSocial from './AppFooterSocial.vue';

export default {
    name: 'AppFooter',
    components:{
        AppFooterLink,
        AppFooterSocial
    }
}
</script>

<template>
    <footer>
        <AppFooterLink></AppFooterLink>
        <AppFooterSocial></AppFooterSocial>
    </footer>
</template>

<style scoped lang="scss"></style>