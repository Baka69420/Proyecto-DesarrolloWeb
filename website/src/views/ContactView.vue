<script>
import ContactInfoApp from '@/components/information/ContactInfoApp.vue'
import EmailFormApp from '@/components/api-connected/EmailFormApp.vue'
import MapApp from '@/components/information/MapApp.vue'

export default {
  components: {
    ContactInfoApp,
    EmailFormApp,
    MapApp
  }
}
</script>

<template>
    <div id="contact-data">
      <div id="contact-info">
        <div id="contact-socials">
          <ContactInfoApp/>
        </div>
        <div id="email-form">
          <EmailFormApp/>
        </div>
      </div>
      <div id="map-location">
        <MapApp/>
      </div>
    </div>
</template>

<style>
#contact-data{
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

#contact-info {
  display: flex;
  gap: 20px;
}

@media only screen and (max-width: 1000px) {
  #contact-info {
    flex-direction: column;
  }

  #contact-info #contact-socials, #contact-info #email-form {
   flex-basis: 100%;
  }
}

@media only screen and (min-width: 1000px) {
  #contact-info {
    flex-direction: row;
  }
  
  #contact-info #contact-socials, #contact-info #email-form {
   flex-basis: 50%;
  }
}
</style>
  

  