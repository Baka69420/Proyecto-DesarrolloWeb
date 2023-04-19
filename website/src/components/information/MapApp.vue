<template>
    <div id="title">
        <h1>Localizacion de la tienda</h1>
    </div>
    <div id="map">
        <iframe src="https://maps.google.com/maps?width=600&amp;height=400&amp;hl=es&amp;q=Pastelillos Carrizal&amp;t=&amp;z=16&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"></iframe>
    </div>
</template>

<style scoped>
#title {
    color: #ffa753;
    text-align: center;
    border-bottom: 2px solid #ffa753;
    margin-bottom: 20px; 
}

#map, #map iframe {
    width: 100%;
    height: 500px;
}
</style>