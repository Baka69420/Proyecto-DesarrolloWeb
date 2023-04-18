<script>
import CarouselApp from '@/components/api-connected/CarouselApp.vue'
import StoreInfoApp from '@/components/information/StoreInfoApp.vue'
//import HotProductsApp from '@/components/information/CarouselApp.vue'

export default {
  components: {
    CarouselApp,
    StoreInfoApp
  }
}
</script>

<template>
  <div id="carrousel">
    <CarouselApp/>
  </div>

  <div id="more-info">
    <div id="store-info">
      <StoreInfoApp/>
    </div>
    <div id="hot-products">

    </div>
  </div>
</template>
