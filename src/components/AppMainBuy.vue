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
            <div class="row justify-content-center g-4 px-5">
                <div v-for="purchase in purchases" class="col-6 col-md d-flex align-items-center">
                    <div class="image me-2">
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

    [class^=col] {
        .image {
            width: 2.5rem;
            height: 2.5rem;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }

        .text{
            font-size: .875rem;
            color: $brand-light;
            text-transform: uppercase;
        }
    }
}
</style>