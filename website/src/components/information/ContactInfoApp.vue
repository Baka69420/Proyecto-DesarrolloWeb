<template>
    <div id="title">
        <h1>Medios de Contacto</h1>
    </div>
    <div id="comm-methods">
        <div class="comm-method">
            <img src="@/assets/images/Facebook.png" alt="Facebook logo">
            <div class="text">
                <h5>Facebook:</h5>
                <p>Pastelillos Carrizal</p>
            </div>
        </div>
        <div class="comm-method">
            <img src="@/assets/images/Instagram.png" alt="Instagram logo">
            <div class="text">
                <h5>Instagram:</h5>
                <p>pastelillos_carrizal_</p>
            </div>
        </div>
        <div class="comm-method">
            <img src="@/assets/images/Whatsapp.png" alt="Whatsapp logo">
            <div class="text">
                <h5>WhatsApp:</h5>
                <p>70745421</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

#comm-methods {
    width: fit-content;
    margin: 0 auto;
}

#comm-methods .comm-method {
    display: flex;
    height: 75px;
    flex-direction: row;
    gap: 10px;
}

#comm-methods .comm-method img {
    height: 60px;
}

#comm-methods .comm-method #text {
    height: fit-content;
    margin: auto 0;
}

</style>