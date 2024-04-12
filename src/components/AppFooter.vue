<script>
export default {
    name: 'AppFooter',
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
    <footer>
        <!-- Link -->
        <div class="footer-link-container">
            <div class="container d-flex justify-content-between">
                <div class="row justify-content-between w-100">
                    <div class="col-12 col-lg-6 footer-link d-flex flex-wrap py-5">
                        <div class="container">
                            <div class="row">
                                <div class="col-4 col-lg-3">
                                    <div class="row">
                                        <div class="col">
                                            <div class="title fs-4">dc comics</div>
                                            <ul>
                                                <li><a href="#">Characters</a></li>
                                                <li><a href="#">Comics</a></li>
                                                <li><a href="#">Movies</a></li>
                                                <li><a href="#">Tv</a></li>
                                                <li><a href="#">Games</a></li>
                                                <li><a href="#">Videos</a></li>
                                                <li><a href="#">News</a></li>
                                            </ul>
                                        </div>
                                        <div class="col">
                                            <div class="title fs-4">shop</div>
                                            <ul>
                                                <li><a href="#">Shop DC</a></li>
                                                <li><a href="#">Shop DC Collectibles</a></li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-4 col-lg-3">
                                    <div class="title fs-4">dc</div>
                                    <ul>
                                        <li><a href="#">Terms Of Use</a></li>
                                        <li><a href="#">Privacy policy (New)</a></li>
                                        <li><a href="#">Ad Choices</a></li>
                                        <li><a href="#">Advertising</a></li>
                                        <li><a href="#">Jobs</a></li>
                                        <li><a href="#">Subscriptions</a></li>
                                        <li><a href="#">Talent Workshops</a></li>
                                        <li><a href="#">CPSC Certificates</a></li>
                                        <li><a href="#">Rating</a></li>
                                        <li><a href="#">Shop Help</a></li>
                                        <li><a href="#">Contact Us</a></li>
                                    </ul>
                                </div>
                                <div class="col-4 col-lg-3">
                                    <div class="title fs-4">sites</div>
                                    <ul>
                                        <li><a href="#">DC</a></li>
                                        <li><a href="#">MAD Magazine</a></li>
                                        <li><a href="#">DC Kids</a></li>
                                        <li><a href="#">DC Universe</a></li>
                                        <li><a href="#">DC Power </a></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-6 footer-img d-none d-lg-block"></div>
                </div>
            </div>
        </div>
        <!-- /Link -->
        <!-- Social -->
        <div class="footer-social">
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
        </div>
        <!-- /Social -->
    </footer>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.footer-link-container {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    
    .row {
        .footer-link {
            .title {
                color: $brand-light;
                text-transform: uppercase;
                font-weight: 900;
            }

            ul {
                a {
                    font-size: .875rem;
                    color: $brand-tertiary;
                    &:hover {
                        color: $brand-primary;
                    }
                }
            }
        }

        .footer-img {
            width: 50%;
            background-image: url(../assets/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-position: center;
            background-size: cover;
        }
    }
}

.footer-social {
    background-color: $brand-secondary-light;
    text-transform: uppercase;
    
    .container {
        button {
            padding: .875rem;
            background-color: $brand-secondary-light;
            border: .0625rem solid $brand-primary;
            color: $brand-light;
            text-transform: uppercase;
            transition: transform 0.5s;
            
            &:hover{
                background-color: $brand-light;
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