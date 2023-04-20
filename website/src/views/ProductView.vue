<script>
import ProductInfoApp from '@/components/api-connected/ProductInfoApp.vue'

export default {
  components: {
    ProductInfoApp,
  },
  props: {
    productID: String,
  }
}
</script>

<template>
    <div id="product">
      <ProductInfoApp :productID="productID" />
    </div>
</template>

<style scoped>
#product{
  padding: 20px;
}
</style>