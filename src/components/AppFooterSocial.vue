<script>
export default {
    name: 'AppFooterSocial',
    data(){
        return {
           images: [
            {
                name: 'Facebook',
                image: 'footer-facebook'
            },
            {
                name: 'Twitter',
                image: 'footer-twitter'
            },
            {
                name: 'Youtube',
                image: 'footer-youtube'
            },
            {
                name: 'Pinterest',
                image: 'footer-pinterest'
            },
            {
                name: 'Periscope',
                image: 'footer-periscope'
            }
           ] 
        };
    },
    methods:{
        getImageUrl(name) {
        return new URL(`../assets/img/${name}.png`, import.meta.url).href
}
    }
}
</script>

<template>
    <section>
        <div class="container d-flex justify-content-between align-items-center py-4">
            <button>Sing-up Now!</button>
            <div class="social d-flex align-items-center gap-3">
                <div class="text">Follow Us</div>
                <div class="social-circle d-flex align gap-2">
                    <div v-for="image in images" class="circle">
                        <img :src="getImageUrl(image.image)" :alt="image.name">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

section {
    background-color: $brand-secondary-light;
    text-transform: uppercase;
    
    .container {
        button {
            padding: 14px;
            background-color: $brand-secondary-light;
            border: 1px solid $brand-primary;
            color: #ffffff;
            text-transform: uppercase;
            transition: transform 0.5s;
            
            &:hover{
                background-color: #ffffff;
                color: $brand-primary;
                font-size: 900;
                transform: scale(1.1);
            }
        }
        
        .social {
            .text {
                color: $brand-primary;
            }

            .social-circle{
                img {
                    cursor: pointer;

                    &:hover {
                        filter: brightness(0.8);
                    }
                }
            }
        }
    }
}
</style>