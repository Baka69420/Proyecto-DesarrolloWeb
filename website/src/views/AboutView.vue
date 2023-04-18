<script>
import StoreHistoryApp from '@/components/information/StoreHistoryApp.vue'
import CreatorInfoApp from '@/components/information/CreatorInfoApp.vue'

export default {
  components: {
    StoreHistoryApp,
    CreatorInfoApp
  }
}
</script>

<template>
  <div id="more-info">
    <div id="store-history">
      <StoreHistoryApp/>
    </div>
    <div id="web-creator">
      <CreatorInfoApp/>
    </div>
  </div>
</template>

<style>
  #more-info{
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
</style>