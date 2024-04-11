<script>
export default {
    name: 'AppFooterLink'
}
</script>

<template>
    <section>
        <div class="container d-flex justify-content-between">
            <div class="footer-link d-flex flex-wrap gap-5 py-5">
                <div class="container">
                    <div class="row">
                        <div class="col">
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
                        <div class="col">
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
                        <div class="col">
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
            <div class="footer-img"></div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

section {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    
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
        width: 563px;
        background-image: url(../assets/img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
    }
}
</style>