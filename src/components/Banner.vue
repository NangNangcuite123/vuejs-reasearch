<template>
    <div class="herobanner d-flex">
        <div class="container position-relative overflow-hidden">
            <div class="row h-100">
                <div class="col-6">
                    <div class="left-content h-100 d-flex align-items-center">
                        <div class="card-content">
                            <h1 class="card-title">Enjoy your <span style="color:#F4AE26;">coffee</span> before your
                                activity</h1>
                            <p class="card-text">Boost your productivity and build your mood with a glass of coffee in
                                the morning </p>
                            <div class="d-flex gap-3">
                                <button class="btn btn-order" type="button">
                                    Order now
                                    <i class="bi bi-cart"></i>
                                </button>
                                <button class="btn btn-menu" type="button">
                                    More menu
                                    <i class="bi bi-journal-text"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-6 ">
                    <div
                        class="right-content h-100 position-relative d-flex flex-wrap align-items-center justify-content-center">
                        <img class="position-absolute img-fluid" src="/image/coffee-beans-pattern-design.png" alt="">
                        <div class="bg-img-brown rounded-circle d-flex align-items-center justify-content-center">
                            <img src="/image/unsplash_PKXAiiy1O4U.png" alt="" class="img-fluid object-fit-cover">
                        </div>
                        <img class="position-absolute top-25" src="/image/Group 4.png" alt="">
                        <img class="position-absolute bottom-25 img-rating" src="/image/rating_product.png" alt="">
                    </div>
                </div>
            </div>
            <img class="position-absolute w-50 img-beans " src="/image/coffee-beans-pattern-design.png" alt="">
        </div>
    </div>
    <div class="container mt-4">
        <h1 class="popular-now mb-5 display-6">Popular <span class="border-bottom border-3 border-warning">Now</span></h1>
    </div>
    <Card />
</template>


<script>
    import Card from './Card.vue';
    export default {
        name: 'Banner',
        components: {
            Card
        }
    }
</script>
<style scoped>
.herobanner {
    background-color: #F6EBDA;
    height: 80vh;
}

.bg-img-brown {
    width: 400px;
    height: 400px;
    background-color: #2F2105;
    position: absolute;
    z-index: 1;
}

.top-25 {
    right: 60%;
    top: 20%;
    z-index: 3;
}
.img-beans {
    bottom: -25%;
    left: 0;
}

.bottom-25 {
    right:8%;
    bottom: 20%;
    z-index: 4;
}

.right-content .img-fluid {
    bottom: 30%;
    z-index: 0;
}

.btn-order {
    background-color: #2F2105;
    color: #FFFF;
    transition: 0.3s ease-in-out;
}

.btn-order:hover {
    background-color: #F4AE26;
    color: #2F2105;
}

.btn-menu {
    color: #F4AE26;
}
.display-6{
    font-weight: 400;
}
</style>