<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <header>
        <nav class="navbar navbar-expand-lg">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/dc-logo.png" alt="DC Logo">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
                    <ul class="navbar-nav mb-2 mb-lg-0">
                        <li class="nav-item me-4">
                            <a class="nav-link ms-active" href="#">Characters</a>
                            <div class="ms-active"></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Comics</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Movies</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Tv</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Games</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Collectibles</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Videos</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">Fans</a>
                            <div></div>
                        </li>
                        <li class="nav-item me-4">
                            <a class="nav-link" href="#">News</a>
                            <div></div>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Shop</a>
                            <div></div>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.navbar-nav {
    text-transform: uppercase;
    .nav-item {
        .nav-link{
            &.ms-active {
                color: $brand-primary;
            }
            &:hover{
            color: $brand-primary;
            }
        }
        div {
            &.ms-active {
                height: 5px;
                background-color: $brand-primary;
            }
        }
    }
}
</style>