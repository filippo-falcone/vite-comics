<script>
import AppFooterLink from './AppFooterLink.vue';

export default {
    name: 'AppFooter',
    components:{
        AppFooterLink
    }
}
</script>

<template>
    <footer>
        <AppFooterLink></AppFooterLink>
    </footer>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
}
</style>