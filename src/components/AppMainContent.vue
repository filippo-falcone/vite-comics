<script>
export default {
    name: 'AppMainContent'
}
</script>

<template>
    <!-- Hero -->
    <section class="hero">
        <img src="../assets/img/jumbotron.jpg" alt="">
    </section>
    <!-- /Hero -->
    <!-- Current Series -->
    <section class="current-series">
        <div class="container pb-5">
            <div class="content-container d-flex flex-column">
                    <div class="title rectangle py-3">
                    <div class="fs-3">current series</div>
                </div>
                <div class="row">
                    
                </div>
                <div class="load-more rectangle py-2 text-center">
                    <div>load more</div>
                </div>
            </div>
        </div>
    </section>
    <!-- /Current Series -->
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.hero {
    height: 25rem;

    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

.current-series {
    background-color: $brand-secondary;
    color: $brand-light;
    text-transform: uppercase;
   
    .content-container{
        margin-top: -35px;

        .rectangle {
            width: fit-content;
            background-color: $brand-primary;
            &.title {
                padding-left: 1.875rem;
                padding-right: 1.875rem;
            }
            
            &.load-more {
                padding-left: 3.75rem;
                padding-right: 3.75rem;
            }
        }
        .load-more {
            align-self: center;
            cursor: pointer;
        }
    }
    
}
</style>