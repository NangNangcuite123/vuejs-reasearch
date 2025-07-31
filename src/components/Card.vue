<template>
  <section class="mt-10">
        <div class="container bg-popular rounded-5 px-4 py-3 position-relative">
            <div class="row">
                <div class="col-lg-4" v-for="(item, index) in drinks" :key="index">
                    <div class="card p-3 bg-white border-0 box-shadow">
                            <img :src="item.image" class="rounded-5 object-fit-cover" alt="Drink image" />
                            <img src="/image/rating_product.png" alt="" class="position-absolute rating-product">
                        <div class="card-body p-0">
                            <div class="d-flex justify-content-between mt-2">
                                <h5 class="card-title fs-4">{{ item.name }}</h5>
                                <h5 class="card-title fs-4">{{ item.price }} K</h5>
                            </div>
                            <div class="d-flex justify-content-between align-items-center">
                                <div class="mt-2">
                                    <button class="btn border px-4 btn-hot">Hot</button>
                                    <button class="btn border px-4 btn-cold ms-3">Cold</button>
                                </div>
                                <a href="#" class="rounded-circle btn-cart d-flex align-items-center justify-content-center">
                                    <i class="bi bi-cart"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <div class="container mt-4">
        <h1 class="popular-now mb-5 display-6 ">How to use delivery <span class="border-bottom border-3 border-warning">service</span></h1>
    </div>
    <section>
        <div class="container">
            <div class="row">
                <div class="col-lg-4" v-for="(service, index) in delivery" :key="index">
                    <div class="card border-0">
                        <div class="card-body">
                            <img :src="service.image" alt="" class="img-fluid m-auto d-block">
                            <h1 class="fs-3 text-center">{{ service.name }}</h1>
                            <p class="fs-10 text-center">{{ service.description }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  data() {
    return {
      drinks: [
        {
          name: "Vanilla Latte",
          price: 21,
          image: "/image/unsplash_RFHFV7lVQBY.png"
        },
        {
          name: "Caramel Macchiato",
          price: 12,
          image: "/image/espresso.png"
        },
        {
          name: "Mocha",
          price: 23,
          image: "/image/hazelnut latte.png"
        }
      ],
      delivery: [
        {
          name: "Choose your coffee",
          description: "there are 20+ coffees for you",
          image: "/image/image.png"
        },
        {
          name: "We delivery it to you",
          description: "Choose delivery service",
          image: "/image/food-truck 1.png"
        },
        {
          name: "Enjoy your coffee",
          description: "Choose delivery service",
          image: "/image/coffee-cup 2.png",
        }
      ]

    };
  }
};
</script>

<style scoped>
.card-title{
    color: #2F2105;
}
.btn-menu:hover {
    background-color: #2F2105;
    color: #FFFF;
}


.box-shadow {
    box-shadow: #bebebe75 0px 3px 8px;
}

.bg-popular {
    background: #F9D9AA;
}
.btn-hot{
    color: #FF902B;
    border-color: #FF902B !important;
}
.btn-hot:hover{
    background-color: #FF902B;
    color: #FFFFFF;
}
.btn-cold{
    color: #FFD28F;
    border-color: #FFD28F !important;
}
.btn-cold:hover{
    background-color: #FFD28F;
    color: #FFFFFF;
}
.rating-product{
    width:100px;
    left: 5%;
    top: 5%;
}
.btn-cart{
    width: 45px;
    height: 45px;
    font-size: 18px;
    color: #fff;
    background-color: #FF902B;
}
.display-6{
    font-weight: 400;
}
img{
    object-fit: cover !important;
}
</style>