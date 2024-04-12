<script>
export default {
    name: 'AppHeader',
    data(){
       return {
        links: ['Characters','Comics','Movies','Tv','Games','Collectibles','Videos','Fans','News','Shop'
        ],
        activeItem: null
       };
    },
    methods: {
        activeLink(index){
            this.activeItem = index;
        }
    }
}
</script>

<template>
    <header>
        <nav class="navbar navbar-expand-xl">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/dc-logo.png" alt="DC Logo">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
                    <ul class="navbar-nav mb-2 mb-lg-0">
                        <li v-for="link, index in links" class="nav-item me-4" @click="activeLink(index)">
                            <a class="nav-link" :class="{'ms-active': index == activeItem}" href="#">{{link}}</a>
                            <div class="d-none d-md-block" :class="{'ms-active': index == activeItem}"></div>
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
            &:hover {
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