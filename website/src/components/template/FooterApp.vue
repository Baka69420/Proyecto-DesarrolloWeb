<template>
  <div id="styling">
      <h5 id="creator">Creado por:<br>Rafael Alvarado</h5>
      <div id="socials">
        <a href="https://www.facebook.com/Pastelilloscarrizal"><img src="@/assets/images/Facebook.png" alt=""></a>
        <a href="https://www.instagram.com/pastelillos_carrizal_/"><img src="@/assets/images/Instagram.png" alt=""></a>
        <a href="https://web.whatsapp.com/send?phone=50670745421"><img src="@/assets/images/Whatsapp.png" alt=""></a>
      </div>
  </div>
</template>

<style scoped>
#styling {
padding: 10px 50px;
display: flex;
text-align: center;
}

#socials{
  margin-left: auto;
}

#socials img {
  height: 50px;
  padding: 0 10px;
}

@media only screen and (max-width: 575px) {
  #styling {
    flex-direction: column;
    gap: 20px;
  }

  #creator {
    margin: 0 auto;
  }

  #socials {
    margin-right: auto;
  }
}

@media only screen and (min-width: 575px) {
  #styling {
    flex-direction: row;
  }
  
  #creator {
    margin: 0 0;
  }

  #socials {
    margin-right: 0;
  }
}
</style>