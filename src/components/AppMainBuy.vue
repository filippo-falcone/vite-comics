<script>
export default {
    name: 'AppMainBuy',
    data(){
        return {
            purchases: [
                {
                    text: 'digital comics',
                    image: 'buy-comics-digital-comics.png'
                },
                {
                    text: 'dc merchandise',
                    image: 'buy-comics-merchandise.png'
                },
                {
                    text: 'subscription',
                    image: 'buy-comics-subscriptions.png'
                },
                {
                    text: 'comic shop locator',
                    image: 'buy-comics-shop-locator.png'
                },
                {
                    text: 'dc power visa',
                    image: 'buy-dc-power-visa.svg'
                }
            ]
        };
    },
    methods: {
        getImageUrl(name) {
            return new URL(`../assets/img/${name}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <section>
        <div class="container py-4">
            <div class="row g-3 px-5">
                <div v-for="purchase in purchases" class="col d-flex align-items-center">
                    <div class="image me-3">
                        <img :src="getImageUrl(purchase.image)" :alt="purchase.text">
                    </div>
                    <a href="#" class="text">{{ purchase.text }}</a>
                </div>
            </div>
        </div>
    </section>
</template>

<style scope lang="scss">
@use '../style/partials/variables' as *;

section {
    background-color: $brand-primary;

    .col {
        .image {
            width: 40px;
            height: 40px;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }

        .text{
            color: #ffffff;
            text-transform: uppercase;

        }
    }
}
</style>