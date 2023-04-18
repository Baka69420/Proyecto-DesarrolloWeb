<template>
  <div id="branding">
    <img src="@/assets/images/logo.png" alt="logo">
    <h1>Pastelillos Carrizal</h1>
  </div>  
  <nav class="navbar sticky-top navbar-expand-sm navbar-light" style="background-color: #fecb70;">
        <div class="container">
          <button class="navbar-toggler d-lg-none" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavId" aria-controls="collapsibleNavId"
              aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="collapsibleNavId">
              <ul class="navbar-nav me-auto mt-2 mt-lg-0">
                  <li class="nav-item">
                      <router-link class="nav-link" :to="{name: 'home'}">Pagina Principal</router-link>
                  </li>
                  <li class="nav-item">
                      <router-link class="nav-link" :to="{name: 'products'}">Productos</router-link>
                  </li>
                  <li class="nav-item">
                      <router-link class="nav-link" :to="{name: 'contact'}">Contacto</router-link>
                  </li>
                  <li class="nav-item">
                      <router-link class="nav-link" :to="{name: 'about'}">Sobre Pagina</router-link>
                  </li>
              </ul>
          </div>
    </div>
  </nav>
</template>

<style scoped>
#branding {
  height: 100px;
  padding: 10px 50px;
  display: flex;
}

#branding * {
  margin: auto 0;
}

#branding img {
  height: 100%;
}

#branding h1 {
  margin-left: auto;
}

@media only screen and (max-width: 575px) {
  #branding img {
    height: 100%;
    margin: 0 auto;
  }

  #branding h1 {
    display: none;
    margin-left: auto;
  }
}

@media only screen and (min-width: 575px) {
  #branding img {
    height: 100%;
  }
  
  #branding h1 {
    display: block;
    margin-left: auto;
  }
}
</style>