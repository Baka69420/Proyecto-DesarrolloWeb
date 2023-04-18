<script>
import HeaderApp from '@/components/HeaderApp.vue'
import FooterApp from '@/components/FooterApp.vue'

export default {
  components: {
    HeaderApp,
    FooterApp
  }
}
</script>

<template>
  <div id="background">
    <div id="content">
      <header>
        <HeaderApp/>
      </header>
      <main>
        <router-view/>
      </main>
      <footer>
        <FooterApp/>
      </footer>
    </div>
  </div>
</template>

<style scoped>
  #content {
    margin: 0 auto;
    background-color: whitesmoke;
  }

  header {
    background-color: #ffa753;
  }

  footer {
    background-color: #fecb70;
  }

  @media only screen and (max-width: 1000px) {
    #content {
      width: 100%;
    }
  }

  @media only screen and (min-width: 1000px) {
    #content {
      width: 70%;
    }
  }
</style>