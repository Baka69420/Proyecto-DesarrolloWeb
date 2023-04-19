<script>
import CarouselApp from '@/components/api-connected/CarouselApp.vue'
import ProductQualityApp from '@/components/information/ProductQualityApp.vue'
import StoreInfoApp from '@/components/information/StoreInfoApp.vue'
import HotProductsApp from '@/components/api-connected/HotProductsApp.vue'

export default {
  components: {
    CarouselApp,
    ProductQualityApp,
    StoreInfoApp,
    HotProductsApp
  }
}
</script>

<template>
  <div id="carrousel">
    <CarouselApp/>
  </div>
  <div id="product-quality">
    <ProductQualityApp/>
  </div>
  <div id="main-info">
    <div id="store-info">
      <StoreInfoApp/>
    </div>
    <div id="hot-products">
      <HotProductsApp/>
    </div>
  </div>
</template>

<style>
#product-quality {
  padding: 20px;
}

#main-info{
  padding: 20px;
  display: flex;
  gap: 20px;
}

@media only screen and (max-width: 1000px) {
  #main-info {
    flex-direction: column;
  }

  #main-info #store-info {
    flex-basis: 100%;
  }

  #main-info #hot-products {
    flex-basis: 100%;
  }
}

@media only screen and (min-width: 1000px) {
  #main-info {
    flex-direction: row;
  }

  #main-info #store-info {
    flex-basis: 70%;
  }

  #main-info #hot-products {
    flex-basis: 30%;
  }
}
</style>
