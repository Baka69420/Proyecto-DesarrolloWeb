<script>
import CarouselApp from '@/components/api-connected/CarouselApp.vue'
import StoreInfoApp from '@/components/information/StoreInfoApp.vue'
import HotProductsApp from '@/components/api-connected/HotProductsApp.vue'

export default {
  components: {
    CarouselApp,
    StoreInfoApp,
    HotProductsApp
  }
}
</script>

<template>
  <div id="carrousel">
    <CarouselApp/>
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
#main-info{
  padding: 20px;
  display: flex;
  gap: 20px;
}

@media only screen and (max-width: 1000px) {
  #main-info {
    flex-direction: column;
  }
}

@media only screen and (min-width: 1000px) {
  #main-info {
    flex-direction: row;
  }
}
</style>
