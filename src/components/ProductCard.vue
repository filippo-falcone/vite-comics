<script>
export default {
    name: 'ProductCard',
    props: {
        cardInfo: Object
    },
    methods: {
        getImageUrl(name) {
            return new URL(`${name}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="col-6 col-md-4 col-lg-3 col-xl-2">
        <div class="img-container">
            <img :src="getImageUrl(cardInfo.thumb)"  :alt="cardInfo.series">
        </div>
        <div class="text pt-4">{{ cardInfo.series }}</div>
    </div>
</template>

<style scoped lang="scss">
.img-container {
    width: 150px;
    height: 150px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

@media screen and (min-width: 576px) {
    .img-container {
        width: 15.625rem;
        height: 15.625rem;
    }
}

@media screen and (min-width: 768px) {
    .img-container {
        width: 13.75rem;
        height: 13.75rem;
    }
}

@media screen and (min-width: 992px) {
    .img-container {
        width: 14.375rem;
        height: 14.375rem;
    }
}

@media screen and (min-width: 1200px) {
    .img-container {
        width: 11.75rem;
        height: 11.75rem;
    }
}
</style>