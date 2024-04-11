<script>
export default {
    name: 'AppMainContent'
}
</script>

<template>
    <section>
        <div class="container py-5">
            <h1 class="text-light">--> Content goes here <---</h1>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

section {
    background-color: $brand-secondary;
}
</style>